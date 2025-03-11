## Test 2


1. Create Topic, test2 with 2 partitions and 1 replica.
```
$ ./kafka-topics.sh --bootstrap-server $BS --create --topic test2 --partitions 2 --replication-factor 1
```
2. Create producer and try to send the data into test2.
```
$ ./kafka-console-producer.sh --bootstrap-server $BS --topic test2
$ ...<type the message you want to send>
```

## Questions

1. What the error message you received while sending the message into test2 ?
2. What is the possible reason to lead the produce issue ?
3. How to address the issue to make the data can be sent successfully ?
