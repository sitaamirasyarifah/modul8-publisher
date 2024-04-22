## Module 8
Nama    : Sita Amira Syarifah

NPM     : 2206023023

Kelas   : Adpro-C

**1. How many data your publisher program will send to the message broker in one run?**

In the publisher program that has been created, the `main` function initializes a publisher `p` for the message broker `CrosstownBus`, then publishes five events of `UserCreatedEventMessage` using the `publish_event` method of that publisher. Therefore, in one run of the program, **the publisher sends five data messages to the message broker**.


**2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?**

The URL "amqp://guest:guest@localhost:5672" is typically used to connect to a message broker using AMQP. If the URL used in both the publisher and subscriber programs is the same, it means that both programs are connected to the same instance of the message broker running on the same machine, using the same authentication credentials and port number as well. This is done to ensure that the publisher can publish messages to the same instance of the message broker where the subscriber is subscribed.
