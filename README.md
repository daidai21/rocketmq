start read commit-id: `50e314eb8ada23283dcdbb261766183c90fd435c`

`git add . && git commit -m "." && git push origin_self 3.0`

### code of examples

重点关注的client：

org.apache.rocketmq.client.consumer.DefaultMQPushConsumer

org.apache.rocketmq.client.consumer.DefaultLitePullConsumer

org.apache.rocketmq.client.producer.DefaultMQProducer

org.apache.rocketmq.client.producer.TransactionMQProducer

### catalog

* [remoting](./remoting) 网络通信模块
    * [RemotingService](./remoting/src/main/java/org/apache/rocketmq/remoting/RemotingService.java)
    * [RemotingClient](./remoting/src/main/java/org/apache/rocketmq/remoting/RemotingClient.java)
    * [RemotingServer](./remoting/src/main/java/org/apache/rocketmq/remoting/RemotingServer.java)
    * [netty](./remoting/src/main/java/org/apache/rocketmq/remoting/netty)
        * [NettyRemotingAbstract](./remoting/src/main/java/org/apache/rocketmq/remoting/netty/NettyRemotingAbstract.java)
        * [NettyRemotingClient](./remoting/src/main/java/org/apache/rocketmq/remoting/netty/NettyRemotingClient.java)
        * [NettyRemotingServer](./remoting/src/main/java/org/apache/rocketmq/remoting/netty/NettyRemotingServer.java)
    * [protocol](./remoting/src/main/java/org/apache/rocketmq/remoting/protocol)
        * [RemotingCommand](./remoting/src/main/java/org/apache/rocketmq/remoting/protocol/RemotingCommand.java)  消息的封装
        * [LanguageCode](./remoting/src/main/java/org/apache/rocketmq/remoting/protocol/LanguageCode.java)
* [client](./client)
    * [consumer](./client/src/main/java/org/apache/rocketmq/client/consumer)
        * [DefaultLitePullConsumer](./client/src/main/java/org/apache/rocketmq/client/consumer/DefaultLitePullConsumer.java)
        * [DefaultMQPushConsumer](./client/src/main/java/org/apache/rocketmq/client/consumer/DefaultMQPushConsumer.java)
          推荐使用的
    * [producer](./client/src/main/java/org/apache/rocketmq/client/producer)
        * [DefaultMQProducer](./client/src/main/java/org/apache/rocketmq/client/producer/DefaultMQProducer.java)
        * [TransactionMQProducer](./client/src/main/java/org/apache/rocketmq/client/producer/TransactionMQProducer.java)
    * [PullMessageService](./client/src/main/java/org/apache/rocketmq/client/impl/consumer/PullMessageService.java)
    * [RebalanceImpl](client/src/main/java/org/apache/rocketmq/client/impl/consumer/RebalanceImpl.java)
    * [RebalanceService](client/src/main/java/org/apache/rocketmq/client/impl/consumer/RebalanceService.java)
    * [TopicPublishInfo](client/src/main/java/org/apache/rocketmq/client/impl/producer/TopicPublishInfo.java)
    * [MQFaultStrategy](client/src/main/java/org/apache/rocketmq/client/latency/MQFaultStrategy.java)
* broker
* namesrv
* [filter](./filter)  消息过滤实现
* [common](./common)
    * [protocol](./common/src/main/java/org/apache/rocketmq/common/protocol)
        * [heartbeat](./common/src/main/java/org/apache/rocketmq/common/protocol/heartbeat)
            * [MessageModel](./common/src/main/java/org/apache/rocketmq/common/protocol/heartbeat/MessageModel.java)




