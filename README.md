### Apache Kafka Fundamentals:
I will try to cover all the fundamentals/main concepts which every developer must aware from Apache Kafka:
- [x] Topoic
- [x] Partition
- [ ] Event
- [ ] Producer
- [ ] Consumer
- [ ] Streams
- [ ] Connect
- [ ] How to run locally

#### Topic:
* It's a streams of related messages/data in `Kafka` or you can say it's similar to table in DB (without constraints)
* We can have as many topic as we want.
* It's identify by it's name.
* `Topic can be split into multiple partitions` OR `Topic can have multiple partitions`
* We can configure that topic can some number of partitions as we want
* [Video desc](https://www.youtube.com/watch?v=kj9JH3ZdsBQ)

#### Partition:
* Partition is nothing just a node of specific topic as we know one topic can have multiple partions for scalling Topic.
* As we know Kafka is distributed system, so we can decide to have many partions for specific topic to handle for high performance.  
* If we want to write mesaages without any order then simply we can push to topic by it's name and Kafka himself by round robin algurithm
it will write messages to different partitions of a topic.
* But if we want to maintain messages order then we need to push message to kafka along with topic name and key (partition) so it will store message in same partion of a topic.
* Each `Message` with in a partition gets an incremental ID called offset 
* [Video desc](https://www.youtube.com/watch?v=y9BStKvVzSs)
> How to run:
* Simply run below command to run Zookeeper and Kafka as docker container

        apache-kafka/kafka-instalation/docker-compose up
        
