## Test 3


1. Create Topic, test3 with 1 partitions and 2 replicas.
```
$ ./kafka-topics.sh --bootstrap-server $BS --create --topic test3 --partitions 1 --replication-factor 2
```
2. Use kafka-producer-perf-test.sh to send numerous data into test3.
```
$ ./kafka-producer-perf-test.sh --topic test3 --num-records 307200000000 --record-size 524288 --throughput -1 --producer-props bootstrap.servers=$BS
```

## Questions

1. Please compare the BK1's CpuUser and BK2's CpuUser metrics, and describe what you observed.
2. What is the possilbe reason ?
3. Do you have any idea to solve the above issue ? e.g update or increase the configuration etc.
