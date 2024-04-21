a. What is amqp? <br>
amqp stands for Advanced Message Queueing Protocol. It is an open standard for passing business messages between applications or organizations. It connects systems, feeds business processes with the information they need and reliably transmits onward the instructions that achieve their goals. Taken from: [What is AMQP](https://www.amqp.org/about/what) <br>
<br>
b. What it means? guest:guest@localhost:5672, what is the first guest, and what is the second guest, and what is localhost:5672 for?

- guest:guest@localhost:5672 is a connection for AMQP server. <Br>
- The first guest in guest:guest is the username for the server <br>
- The second guest in guest:guest is the password for the server <Br>
- localhost:5672 is for defining where the host, in this case the hostname of the server, and which port it listens to, in this case 5672, which is the default port for AMQP.

Chart screenshot
![image](https://github.com/steven-fo/advprog-module8-subscriber/assets/119484321/88d6ac9e-d688-4909-bd23-36de24ac150a)
It can be seen from the image above that there are a number of messages that can't be processed immediately resulting in an increase number of messages inside the queue (almost hit 30 messages). This happens because the subscriber can't receive messages immediately (thread sleep for 1 second).

Chart screenshot
![image](https://github.com/steven-fo/advprog-module8-subscriber/assets/119484321/aad02dbb-4002-4352-adef-f6a5d6aed110)
It can be seen from the chart that this time, the spike reduces quicker than before. This is caused by an increase number in the subscriber.

Subscriber screenshot
![image](https://github.com/steven-fo/advprog-module8-subscriber/assets/119484321/f499ec59-66cd-4ac6-a76c-225fc8b6e09b)
![image](https://github.com/steven-fo/advprog-module8-subscriber/assets/119484321/7dee3858-06bf-49a3-83be-9196b9f58d7d)
![image](https://github.com/steven-fo/advprog-module8-subscriber/assets/119484321/fb5295e1-f46c-4eaf-9de7-d73cfd613b97)

#### Thing to improve
- add get handler action function inside MessageHandler class (compiler told me to do so)
- don't repeat yourself (in the main function in publisher folder, we create 5 instances from publish event function manually, which means there are 5 identical codes but different values)
