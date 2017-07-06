## TERAGEN

```
[root@ip-172-31-9-138 ec2-user]# su - neymar
[neymar@ip-172-31-9-138 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -Ddfs.blocksize=16M -Dmapred.map.tasks=8 655360 /user/neymar/tgen640
17/07/06 12:05:43 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-13-192.eu-central-1.compute.internal/172.31.13.192:8032
17/07/06 12:05:44 INFO terasort.TeraGen: Generating 655360 using 8
17/07/06 12:05:44 INFO mapreduce.JobSubmitter: number of splits:8
17/07/06 12:05:44 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/07/06 12:05:44 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1499356658257_0001
17/07/06 12:05:44 INFO impl.YarnClientImpl: Submitted application application_1499356658257_0001
17/07/06 12:05:44 INFO mapreduce.Job: The url to track the job: http://ip-172-31-13-192.eu-central-1.compute.internal:8088/proxy/application_1499356658257_0001/
17/07/06 12:05:44 INFO mapreduce.Job: Running job: job_1499356658257_0001
17/07/06 12:05:51 INFO mapreduce.Job: Job job_1499356658257_0001 running in uber mode : false
17/07/06 12:05:51 INFO mapreduce.Job:  map 0% reduce 0%
17/07/06 12:05:59 INFO mapreduce.Job:  map 25% reduce 0%
17/07/06 12:06:00 INFO mapreduce.Job:  map 38% reduce 0%
17/07/06 12:06:01 INFO mapreduce.Job:  map 63% reduce 0%
17/07/06 12:06:03 INFO mapreduce.Job:  map 100% reduce 0%
17/07/06 12:06:03 INFO mapreduce.Job: Job job_1499356658257_0001 completed successfully
17/07/06 12:06:03 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1021496
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=677
                HDFS: Number of bytes written=65536000
                HDFS: Number of read operations=32
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=8
                Other local map tasks=8
                Total time spent by all maps in occupied slots (ms)=55198
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=55198
                Total vcore-milliseconds taken by all map tasks=55198
                Total megabyte-milliseconds taken by all map tasks=56522752
        Map-Reduce Framework
                Map input records=655360
                Map output records=655360
                Input split bytes=677
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=506
                CPU time spent (ms)=19940
                Physical memory (bytes) snapshot=1768071168
                Virtual memory (bytes) snapshot=12534919168
                Total committed heap usage (bytes)=2373976064
                Peak Map Physical memory (bytes)=256016384
                Peak Map Virtual memory (bytes)=1580503040
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=1408100361519672
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=65536000

real    0m22.482s
user    0m5.597s
sys     0m0.254s
[neymar@ip-172-31-9-138 ~]$


## Directory Output

```

[neymar@ip-172-31-9-138 ~]$ hdfs dfs -ls /user/neymar/tgen640
Found 9 items
-rw-r--r--   3 neymar ronaldo          0 2017-07-06 12:06 /user/neymar/tgen640/_SUCCESS
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:05 /user/neymar/tgen640/part-m-00000
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:05 /user/neymar/tgen640/part-m-00001
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:05 /user/neymar/tgen640/part-m-00002
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:06 /user/neymar/tgen640/part-m-00003
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:06 /user/neymar/tgen640/part-m-00004
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:06 /user/neymar/tgen640/part-m-00005
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:05 /user/neymar/tgen640/part-m-00006
-rw-r--r--   3 neymar ronaldo    8192000 2017-07-06 12:05 /user/neymar/tgen640/part-m-00007




```


## Blocks

```

[neymar@ip-172-31-9-138 ~]$ hadoop fsck /user/neymar
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-13-192.eu-central-1.compute.internal:50070
FSCK started by neymar (auth:SIMPLE) from /172.31.9.138 for path /user/neymar at Thu Jul 06 12:09:43 EDT 2017
.........Status: HEALTHY
 Total size:    65536000 B
 Total dirs:    3
 Total files:   9
 Total symlinks:                0
 Total blocks (validated):      8 (avg. block size 8192000 B)
 Minimally replicated blocks:   8 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Thu Jul 06 12:09:43 EDT 2017 in 5 milliseconds


The filesystem under path '/user/neymar' is HEALTHY





```
