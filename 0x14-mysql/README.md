# 0x14. MySQL 

<p align="center">
  <img src="https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/280/KkrkDHT.png"
</p>

## Resource

- [What is a database](https://searchdatamanagement.techtarget.com/definition/database)
- [What is a database primary/replicate cluster](https://www.digitalocean.com/community/tutorials/how-to-choose-a-redundancy-plan-to-ensure-high-availability#sql-replication)
- [MySQL primary/replicate setup](https://www.digitalocean.com/community/tutorials/how-to-set-up-replication-in-mysql)
- [Build a robust database backup strategy](https://www.databasejournal.com/ms-sql/developing-a-sql-server-backup-strategy/)
- [Privileges Provided by MySQL](https://dev.mysql.com/doc/refman/8.0/en/privileges-provided.html#priv_replication-client) (***Replication Client***)
- [Creating User for Replication](https://dev.mysql.com/doc/refman/8.0/en/replication-howto-repuser.html)
- [Setting up replicas](https://dev.mysql.com/doc/refman/5.7/en/replication-setup-replicas.html) (***MySQL 5.7.x***)

## Tasks

<details>
<summary>0. Install MySQL</summary><br>
<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/wMPwtg5K/image.png' border='0' alt='image'/></a>
</details>

<details>
<summary>1. Let us in!</summary><br>

<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/zB1QFncd/image.png' border='0' alt='image'/></a>
```sh
mysql> CREATE USER 'holberton_user'@'localhost' IDENTIFIED BY 'projectcorrection280hbtn';
mysql> GRANT REPLICATION CLIENT ON *.* to 'holberton_user'@'localhost';
mysql> FLUSH PRIVILEGES;
```

</details>

<details>
<summary>2. If only you could see what I've seen with your eyes</summary><br>

<a href='https://postimages.org/' target='_blank'><img src='https://i.postimg.cc/sgDm766T/image.png' border='0' alt='image'/></a>
```sh

