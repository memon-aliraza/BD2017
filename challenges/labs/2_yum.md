## Challenge 2: Install latest Cloudera Manager 

```
[root@ip-172-31-9-138 ec2-user]# ls /etc/yum.repos.d

cloudera-manager.repo  mysql-community-source.repo  redhat-rhui-client-config.repo  rhel-source.repo
mysql-community.repo   redhat.repo                  redhat-rhui.repo                rhui-load-balancers.conf
```

## Cloudera Manager Repo FIle

```
[root@ip-172-31-9-138 ec2-user]# cat /etc/yum.repos.d/cloudera-manager.repo

[cloudera-manager]
name = Cloudera Manager, Version 5.11.1
baseurl = https://archive.cloudera.com/cm5/redhat/6/x86_64/cm/5.11.1/
gpgkey = https://archive.cloudera.com/redhat/cdh/RPM-GPG-KEY-cloudera
gpgcheck = 1


```
