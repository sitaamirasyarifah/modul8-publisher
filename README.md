## Module 8
Nama    : Sita Amira Syarifah

NPM     : 2206023023

Kelas   : Adpro-C

**1. How many data your publisher program will send to the message broker in one run?**

In the publisher program that has been created, the `main` function initializes a publisher `p` for the message broker `CrosstownBus`, then publishes five events of `UserCreatedEventMessage` using the `publish_event` method of that publisher. Therefore, in one run of the program, **the publisher sends five data messages to the message broker**.


**2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?**

The URL "amqp://guest:guest@localhost:5672" is typically used to connect to a message broker using AMQP. If the URL used in both the publisher and subscriber programs is the same, it means that both programs are connected to the same instance of the message broker running on the same machine, using the same authentication credentials and port number as well. This is done to ensure that the publisher can publish messages to the same instance of the message broker where the subscriber is subscribed.

**Running RabbitMQ as message broker.**
![rabbitmq](https://github.com/sitaamirasyarifah/modul8-publisher/assets/122429830/7ab6e490-e323-4b76-aef0-620775669054)

**Sending and processing event.**
![Screenshot (460)](https://github.com/sitaamirasyarifah/modul8-publisher/assets/122429830/3b09f4af-cb65-41b4-8257-462d15a08d17)


**Publisher Console**
![publisher](https://github.com/sitaamirasyarifah/modul8-publisher/assets/122429830/eb57a427-7959-4db2-8f50-904e4a26c534)

**Subscriber Console**
![subscriber](https://github.com/sitaamirasyarifah/modul8-publisher/assets/122429830/41d8a1c0-cd9b-4407-9830-8bc00f2081b7)

The images above show that after the publisher application is executed, it will send hardcoded data within the code to the message queue. Subscribers connected to the message queue will receive data from the message queue and print it on the console according to the code that has been created.

**Monitoring chart based on publisher.**
![Screenshot (458)](https://github.com/sitaamirasyarifah/modul8-publisher/assets/122429830/e370e9f2-c591-4e67-a93a-a353f09c0eed)

The image above was obtained after performing the third cargo run compared to the initial one. The graph illustrates an increase in message rate at certain time intervals. This increase is associated with the execution of cargo run on the publisher. It can be observed that each time the publisher is implemented, there is an increase in message throughput on RabbitMQ, which serves as the message queue.