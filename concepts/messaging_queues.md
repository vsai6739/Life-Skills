# What are Messaging Queues?

- Messaging Queues are an asynchronous way of communicating between services.
- They are mainly used in Microservices.
- Messaging queues remove the load from the services.
- Using a Messaging queue, services don't have to wait for the task to be completed.
- Messages are stored in a Queue until they are processed.
- Each message is processed by only one consumer.
- Messaging Queue works based on the producer-consumer model:
    - **Producer**: The service that sends data into the queue.
    - **Consumer**: The service that handles the data sent into the queue.

![Messaging Queue Process](https://d1.awsstatic.com/product-marketing/Messaging/sqs_seo_queue.1dc710b63346bef869ee34b8a9a76abc014fbfc9.png)

In the above image, the Producer is sending a message to the messaging queue, which stores the message temporarily until it is processed by the Consumer. The Consumer communicates with the messaging queue to check for any messages to process. Once the Consumer receives the message, the messaging queue removes that message from the queue.

# Why are they used?

- **Asynchronous Processing**:
    - Producers and Consumers can work independently.
    - They don't have to work at the same time.

- **Scalability**:
    - Multiple Consumers can read from the queue, allowing the system to handle higher loads.

- **Load Balancing**:
    - As multiple Consumers can read from the queue, the load is evenly distributed.

# What are popular tools?

- **RabbitMQ**:
    - An open-source message broker that supports messaging protocols and features like load balancing, routing, and message acknowledgment.

- **Apache Kafka**:
    - Works well for high-throughput data pipelines and event streaming.

- **Amazon SQS (Simple Queue Service)**:
    - A messaging service provided by AWS, designed for building and scaling applications in the cloud.

# What is Enterprise Message Bus?

Enterprise Message Bus (EMB) is a centralized communication system that enables different services and applications to communicate with each other seamlessly.

It acts as an intermediary layer that manages the flow of messages.

For example, consider an application like Amazon that performs multiple tasks. When a customer places an order, the Order Service communicates with the Enterprise Message Bus (EMB).

- The EMB routes this message to the correct consumer based on routing rules.
- The consumer then receives the message from the EMB and processes the request.

![Enterprise Message Bus](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/ESB.svg/220px-ESB.svg.png)

In the above image, we can see that there are multiple producers sending different types of messages. The Enterprise Message Bus (EMB) accepts various messages from different producers and routes them to the correct consumer.

# References

- [Messaging Queues](https://aws.amazon.com/message-queue/)
- [RabbitMQ](https://risingwave.com/blog/the-ultimate-guide-to-top-messaging-queue-tools-in-2024/)
- [Apache Kafka](https://risingwave.com/blog/the-ultimate-guide-to-top-messaging-queue-tools-in-2024/)
- [Amazon SQS](https://risingwave.com/blog/the-ultimate-guide-to-top-messaging-queue-tools-in-2024/)
- [Enterprise Service Bus (ESB)](https://en.wikipedia.org/wiki/Enterprise_service_bus)
