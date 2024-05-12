<img src=./onfire.gif width=50%>

# ImagePress requests failure report
Last week, it was reported that the ImagePress platform was returning 500 Error on all requests made on the platform routes, all the services were down.  90% of the users were affected. The root cause was the failure of our master server web-01.

## Timeline
The error was realized on Monday May 6 10:00 hours (West Africa Time) when our Site Reliability Engineer, Ms Otolorin saw the master server lagging in speed. She immediately disconnected the master server web-01 for further system analysis and channelled all requests to client server web-02. Eventually, this issue was successfully resolved at 12:00 hours same day.

## Root cause and resolution
The ImagePress platform is served by 2 ubuntu cloud server. The master server web-01 was connected to serve all requests, and it stopped functioning due to memory outage as a results of so many requests because during a previous test, the client server web-02 was disconnected temporarily for testing and was not connected to the load balancer afterwards. 

The issue was fixed when the master server was temporarily disconnected for memory clean-up then connected back to the loadbalancer and round-robin algorithm was configured so that both the master and client servers can handle equal amount of requests.

## Measures against such problem in future
- Choose the best loadbalancing algorithm for your programs
- Always keep an eye on your servers to ensure they are running properly
- Have extra back-up servers to prevent your program fro completely going offline during an issue
