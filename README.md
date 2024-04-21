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
