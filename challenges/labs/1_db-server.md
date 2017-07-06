## MySQL Server Information

``` [root@ip-172-31-9-138 ec2-user]# mysql -u root -p -e "select host from information_schema.processlist" 

+-----------+
| host      |
+-----------+
| localhost |
+-----------+
```

## Hostname

```
[root@ip-172-31-9-138 ec2-user]# hostname
ip-172-31-9-138.eu-central-1.compute.internal

```

## Version
```
[root@ip-172-31-9-138 ec2-user]# mysql -u root -p -e "SHOW VARIABLES LIKE 'version'"

+---------------+--------+
| Variable_name | Value  |
+---------------+--------+
| version       | 5.6.36 |
+---------------+--------+
```

## List of Databases

```
[root@ip-172-31-9-138 ec2-user]# mysql -u root -p -e "SHOW DATABASES"
Enter password:
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hmon               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
```
