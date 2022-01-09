# NoSQL and advanced patterns

# Distributed Caching with Redis
Redis (Remote DIctionary Server) is an open-source, networked, single-threaded, in-memory, advanced key-value store with optional durability.

## Home task
### Learn Redis fundamentals
Check out the materials in the sections below, explore the examples. If necessary, ask your mentor for help in understanding.
### Create a free online Redis account
You may use either of the options below, or create a Redis cluster in the cloud shall you have spare credits.
- https://redis.com/redis-enterprise-cloud/pricing/
- https://redistogo.com/
### Refactor caching middleware
Once you have established and tested the connection to your Redis cluster, please refactor the caching middleware you created in Module #2 so that the image is now stored in Redis.

## Additional reading
- Distributed caching in ASP.NET Core: https://docs.microsoft.com/en-us/aspnet/core/performance/caching/distributed
- Redis with .NET: https://docs.redis.com/latest/rs/references/client_references/client_csharp/
- Azure Cache for Redis: https://docs.microsoft.com/en-us/azure/azure-cache-for-redis/cache-dotnet-core-quickstart

## Additional lectures (videos)
- Using Redis as a .NET Core Data Store: https://docs.microsoft.com/en-us/shows/on-net/using-redis-as-a-net-core-data-store

# Data Resilience with MongoDB
MongoDB is an open-source document database built on a horizontal scale-out architecture that uses a flexible schema for storing data.

## Home task
### Learn MongoDB fundamentals
Check out the materials in the sections below, explore the examples. If necessary, ask your mentor for help in understanding.
### Create a free online MongoDB account
You may use either of the options below, or create a cluster in the cloud shall you have spare credits.
- https://www.mongodb.com/cloud/atlas/lp/try2
- https://mlab.com/plans/pricing/#plan-type=sandbox
### Develop 'Reviews' feature
A user may read and leave reviews on the 'Product Details' page. Each review consists of a username, comment, rating (1 to 5), and a timestamp (set by a system). Each authorized user may only write one review. This feature is powered by MongoDB as persistent storage. For now, all reviews should be read from and written to MongoDB directly. You may design this feature as simplest as possible.
Please get familiar with this guide on some practices for building resilient applications: https://docs.opsmanager.mongodb.com/current/reference/resilient-application/. Follow those recommendations while developing your service.

## Additional reading
- MongoDB: https://docs.microsoft.com/en-us/learn/modules/cmu-case-study-nosql-databases/2-mongodb
- Create a web API with ASP.NET Core and MongoDB: https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mongo-app
- MongoDB C#/.NET Driver: https://docs.mongodb.com/drivers/csharp/

## Additional lectures (videos)
- Connecting to a data store: https://docs.microsoft.com/en-us/shows/beginners-series-to-web-apis/connecting-to-a-data-store-11-of-18--beginners-series-to-web-apis

# Microservices and Messaging
In modern architectures, applications are decoupled into smaller, independent building blocks that are easier to develop, deploy and maintain. Message queues provide communication and coordination for these distributed applications. We'll learn how to use RabbitMQ as a message broker.

## Home task
### Learn message-based communication principles and RabbitMQ fundamentals
Check out the materials in the sections below, explore the examples. If necessary, ask your mentor for help in understanding.
### Decouple Reviews microservice
The service that enables posting (i.e., creating) reviews should be decoupled from the primary solution and operate as a standalone console app.
### Employ a message broker
Asynchronous communication between the two services should be established through RabbitMQ: the primary service enqueues a new message to be further dequeued by the Reviews microservice. The message should contain the review entity and the associated metadata (e.g., creation time). The mechanism to fetch reviews should remain unchanged at this time.

## Additional reading
- Communication in a microservice architecture: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/communication-in-microservice-architecture
- Asynchronous message-based communication: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/asynchronous-message-based-communication
- RabbitMQ Use cases: Explaining message queues and when to use them: https://www.cloudamqp.com/blog/rabbitmq-use-cases-explaining-message-queues-and-when-to-use-them.html
- RabbitMQ tutorial - "Hello World!": https://www.rabbitmq.com/tutorials/tutorial-one-dotnet.html
- Implementing an event bus with RabbitMQ for the development or test environment: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/rabbitmq-event-bus-development-test-environment
