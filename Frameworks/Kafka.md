#Kafka
## Introduction
This is basically a Publish-Subscribe framework.
It was created by Linkedin in 2010 and then was made opensource for people.
Kafka framework consists of brokers which are kafka nodes, producers and consumers for producing and consuming messages.

## Storage
Kafka stores data/messages in Topics.
Each topic consist of multiple partitions.
Messages are stored in partitions and are allotted an offset value.
Message can be uniquely identified using topic name + partition name + offset name.
Kafka topics are durable and can store messages as per configured value of TTL or storage.
Messages in a partition are always ordered.
Messages can have metadata key which could be used to decide partition for a message.

## Clustering
Every partition has a leader topic and all the read/write is made to leader topic and then propogated to other topics.
Kafka also has concept of consumer groups which could be used to scale consumption of messages.
Each consumer group consists of multiple consumers and consumers in a consumer group read from different partitions to ensure they do not read duplicate messages.
Adding more partitions and consumer group can help in scaling.
Kakfa can be configured to use in different ways to trade off on consistency and availability.


