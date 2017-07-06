## User Directory 

 ```
[root@ip-172-31-9-138 ec2-user]# hdfs dfs -ls /user
Found 6 items
drwxrwxrwx   - mapred hadoop              0 2017-07-06 11:34 /user/history
drwxrwxr-t   - hive   hive                0 2017-07-06 11:35 /user/hive
drwxrwxr-x   - hue    hue                 0 2017-07-06 11:35 /user/hue
drwxr-xr-x   - hdfs   supergroup          0 2017-07-06 11:45 /user/neymar
drwxrwxr-x   - oozie  oozie               0 2017-07-06 11:35 /user/oozie
drwxr-xr-x   - hdfs   supergroup          0 2017-07-06 11:45 /user/ronaldo
[root@ip-172-31-9-138 ec2-user]#

 
 ```
 
 ##  CM API 
 
 ```
 [root@ip-172-31-9-138 ec2-user]# curl -u admin:admin 'ip-172-31-9-138.eu-central-1.compute.internal:7180/api/v14/hosts'
{
  "items" : [ {
    "hostId" : "decac280-eedb-4cb6-8b3d-17ee01bb60ee",
    "ipAddress" : "172.31.13.192",
    "hostname" : "ip-172-31-13-192.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-9-138.eu-central-1.compute.internal:7180/cmf/hostRedirect/decac280-eedb-4cb6-8b3d-17ee01bb60ee",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "3531671d-c8e1-4220-b5bc-f5740f9d7fb8",
    "ipAddress" : "172.31.2.111",
    "hostname" : "ip-172-31-2-111.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-9-138.eu-central-1.compute.internal:7180/cmf/hostRedirect/3531671d-c8e1-4220-b5bc-f5740f9d7fb8",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "a81b9b42-5993-431a-a2b5-1aa564c1ff1e",
    "ipAddress" : "172.31.4.125",
    "hostname" : "ip-172-31-4-125.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-9-138.eu-central-1.compute.internal:7180/cmf/hostRedirect/a81b9b42-5993-431a-a2b5-1aa564c1ff1e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "00430149-1a1e-4465-8029-771731950a80",
    "ipAddress" : "172.31.6.172",
    "hostname" : "ip-172-31-6-172.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-9-138.eu-central-1.compute.internal:7180/cmf/hostRedirect/00430149-1a1e-4465-8029-771731950a80",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  }, {
    "hostId" : "41740d05-844b-4170-896f-94737a57c353",
    "ipAddress" : "172.31.9.138",
    "hostname" : "ip-172-31-9-138.eu-central-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-9-138.eu-central-1.compute.internal:7180/cmf/hostRedirect/41740d05-844b-4170-896f-94737a57c353",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15664758784
  } ]
}[root@ip-172-31-9-138 ec2-user]#
 ```
 
