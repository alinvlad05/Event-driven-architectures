# Event-driven Architectures

Event-driven architectures are distributed systems that interact with each other by producing and consuming events.

- An event is something relevant that happened in a system.
- In the pub/sub model, producers publish events, which are sent to all subscribers to be consumed.
- Event processing platforms like RabbitMQ and Kafka are responsible for collecting events from the producers, routing, and distributing them to the interested consumers.
- In the AMQP protocol, producers send messages to an exchange in a broker that forwards them to queues according to specific routing algorithms.
- In the AMQP protocol, consumers receive messages from the queues in the broker.
- In the AMQP protocol, messages are data structures composed of key/value attributes and a binary payload.

RabbitMQ is a message broker based on the AMQP protocol that you can use to implement event-driven architectures based on the pub/sub model.

- RabbitMQ provides high availability, resilience, and data replication.

Spring Cloud Function enables you to implement your business logic using the standard Java Function, Supplier, and Consumer interfaces.

- Spring Cloud Function wraps your function and provides several exciting features like transparent type conversion and function composition.
- Functions implemented in the context of Spring Cloud Function can be exposed and integrated with external systems in different ways.
- Functions can be exposed as REST endpoints, packaged, and deployed in a FaaS platform as serverless applications (Knative, AWS Lambda, Azure Function, Google Cloud Functions), or they can be bound to message channels.

Spring Cloud Stream, built on top of Spring Cloud Function, provides you with all the necessary plumbing to integrate your functions with external messaging systems like RabbitMQ or Kafka.

- Once you implement your functions, you don’t have to make any changes to your code. You only need to add a dependency on Spring Cloud Stream and configure it to adapt to your needs.
- In Spring Cloud Stream, destination binders provide integration with external messaging systems.
- In Spring Cloud Stream, destination bindings (input and output) bridge the producers and consumers in your applications with exchanges and queues in a message broker like RabbitMQ.
- Functions and consumers are activated automatically when new messages arrive.
- Suppliers need to be explicitly activated, such as by explicitly sending a message to a destination binding.
