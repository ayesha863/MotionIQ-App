data_fetcher_mobile for MotionIQ

Simple and Beautiful App for fetching and send sensor's data to server.
Steps :
First, you have to set the rabbitmq server's address and port in application.

Then, select appropriate sensors to send data.

click start button to send data.


Note :
Don't forget to follow the following guide lines to start the application successfully.


Platform Server

Overview
A step-by-step guide for setting up a MotionIQ Human Activity Recognition System using RabbitMQ and an Android app. Data is transmitted from a mobile device to RabbitMQ queues and processed by a Java-based consumer.

Features
📱 Real-time data from mobile sensors
🧠 Activity recognition pipeline
🐇 RabbitMQ message brokering
💻 Java consumer backend
Setup Guide
🔧 Installing RabbitMQ
Download the installer from RabbitMQ Downloads
Install and run the server
Enable management UI:
cd "C:\Program Files\RabbitMQ Server\rabbitmq_server-{version}\sbin"
rabbitmq-plugins enable rabbitmq_management
Access the UI: http://localhost:15672
👤 Create a User
Go to Admin > Add a user
Set:
Username: test
Password: test
Tags: administrator
Assign permissions
Note: Guest user can't connect remotely.

🖥️ Running Consumer
Required Files
SensorDataConsumer.java
amqp-client-5.21.0.jar
slf4j-api-2.0.13.jar
slf4j-simple-2.0.13.jar
Steps
javac SensorDataConsumer.java
java SensorDataConsumer
Check RabbitMQ UI under Connections tab to verify.

🔒 Firewall Setup
Open ports 15672 and 5672 in Windows Firewall.

📱 Android App Setup
Install the mobile app.
Enter:
IP address of RabbitMQ server
Port: 5672
Username: test
Select sensors via UI
Using Android Studio
Extract and open the project
Check sendDataService file for credentials
Run the app on a device with USB/Wi-Fi debugging enabled
✅ Testing
Run RabbitMQ server and consumer
Start app and begin data transmission
Monitor logs and RabbitMQ Queues tab for activity
Contributing
All contributions are welcome! Feel free to fork, raise issues, or submit PRs.
