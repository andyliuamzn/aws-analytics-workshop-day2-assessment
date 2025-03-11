## Test 1


1. Create Topic, test1 with 2 partitions and 2 replicas.
```
$ export BS=<your-broker-endpoint>
$ ./kafka-topics.sh --bootstrap-server $BS --create --topic test1 --partitions 2 --replication-factor 2
$ ./kafka-configs.sh --bootstrap-server $BS --entity-type topics --entity-name test1 --alter --add-config compression.type=producer
```

2. Get the detailed output from Topic, test1 to understand what the retention config that we set for the topic.
```
$ ./kafka-topics.sh --bootstrap-server $BS --describe --topic test1
```

3. Send around 1.5 GB data into test1.
```
$ ./kafka-producer-perf-test.sh --topic test1 --num-records 3072 --record-size 524288 --throughput -1 --producer-props bootstrap.servers=$BS
```

4. Use kafka-log-dirs.sh to check what the size of data we have on Topic test1.
```
$ ./kafka-log-dirs.sh --bootstrap-server $BS --topic-list test1 --describe
```

## Questions

1. Please take the screenshot of the kafka-log-dirs.sh result and try to explain it.  
2. What is the data size of the Topic test1 ?
3. Wait for 10 mins and try to execute the kafka-log-dirs.sh command again to check if the retention policy works or not.
4. Please describe what the final result is in Question 3 and explain why we get the result like that.
