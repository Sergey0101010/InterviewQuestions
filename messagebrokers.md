# Message brokers

### What are main architectural components in kafka?
1. Kafka Producer. The producer is a source of data. It does not send messages directly to 
consumer, rather pushes messages to kafka server or broker. Multiple producers can send a message
to the same kafka topic or different kafka topics.
2. Kafka consumer. The consumer acts as receiver, it is responsible for receiving or 
consuming a message. The consumer requests messages from kafka broker. If the kafka consumer
will have enough permissions, then it gets a message from kafka broker.
3. Kafka Broker. The kafka broker is nothing but just a server. It just an intermediate entity
which helps in message exchange between a producer and a consumer. In the kafka cluster 
there are might be one or more kafka brokers.
4. Kafka cluster. It is a group of brokers. There are exist Single broker cluster and 
Multi-broker cluster.
5. Kafka topic. It is a unique name given to data stream or a message stream. On single broker
there can be multiple topics, when producer sends some message it sends it via unique name
which is called topic for a message stream. If consumer wants to consume some message, then
it subscribes to the topic present in kafka broker.
6. Kafka partitions. If we have large volumes of data it is very challenging for the broker
to store data on a single machine. Because kafka is a distributed system we break Kafka topic
in partitions and distribute different partitions into multiple machines. We can configure
number of partitions
7. Offsets. Sequence number is assigned to each message in each partition of a Kafka topic.
This sequence number is called offset. At start, offset points to first message in partition,
when consumer reads message offset pointer moves to the next message.
8. Kafka consumer group. It is a multiple consumers combined to share the workload.
There can be multiple consumer groups subscribing to the same or different topics.

### What is offset in kafka?
In partitions, messages are assigned a unique id number called offset. The role of offset 
is to identify each message in the partition uniquely.
Internally, Kafka writes messages to logs, and the kafka offset represents a position
of a message within that partition's log. It indicates how far the message is from the
beginning of the partition log.

### What is ZooKeeper?
Zookeeper is a top-level software that acts as a centralized service and is used to maintain
naming and configuration data to provide flexible and robust synchronization withing 
distributed systems. Zookeeper keeps track of status of the Kafka cluster nodes and also 
keeps track of Kafka topics, partitions etc.
Zookeeper acts as shared configuration service within the system, and it is necessary for Apache Kafka
Main functions for which Zookeeper is responsible:
- Controller election. The controller is one of the most important broking entities in a Kafka
ecosystem, and it is also has the responsibility to maintain leader-follower relationship
across all the partitions. If a node by some reason is shutting down, the controller
responsibility to tell all the replicas to act as partition leaders.
- Configuration of topics. List of existing topics, number of partitions in each topic, location
of all the replicas etc
- Access control lists
- Membership of the cluster

### What does follower and leader in kafka mean?
One server in partition acts as a leader and one or more act as a follower. The leader
assigns itself tasks that read and write partition requests. Followers follow the leader
and replicate what is being told.

### How does Kafka communicate with servers and clients?
Kafka uses binary protocol which is build on top of TCP

