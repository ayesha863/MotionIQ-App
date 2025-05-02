Here’s a clean, professional, and concise GitHub README description for your **`data_fetcher_mobile`** app (MotionIQ), keeping it well-organized and suitable for your GitHub repo:

---

# MotionIQ – Data Fetcher Mobile

**MotionIQ** is a simple and elegant Android app for collecting sensor data (accelerometer, gyroscope, magnetometer) and sending it to a RabbitMQ server for real-time human activity recognition (HAR).

## 🚀 Features

* 📱 Real-time mobile sensor data transmission
* 🧠 Integration with activity recognition pipelines
* 🐇 RabbitMQ-based message brokering
* 💻 Java-based backend consumer

## 📦 How to Use

1. Set the RabbitMQ server's IP address and port in the app.
2. Select desired sensors via the app UI.
3. Tap the **Start** button to begin data transmission.

> ⚠️ **Important**: Follow setup guidelines carefully for successful operation.

---

## 🛠 Platform Setup Guide

### 1. RabbitMQ Installation

* Download from [RabbitMQ Downloads](https://www.rabbitmq.com/download.html)
* Enable management UI:

  ```bash
  cd "C:\Program Files\RabbitMQ Server\rabbitmq_server-{version}\sbin"
  rabbitmq-plugins enable rabbitmq_management
  ```
* Access UI at: `http://localhost:15672`

### 2. Create User

* Username: `test`
* Password: `test`
* Tags: `administrator`
* Note: Guest users can't connect remotely.

### 3. Java Consumer Setup

**Required files:**

* `SensorDataConsumer.java`
* `amqp-client-5.21.0.jar`
* `slf4j-api-2.0.13.jar`
* `slf4j-simple-2.0.13.jar`

**Run steps:**

```bash
javac SensorDataConsumer.java
java SensorDataConsumer
```

### 4. Firewall

Ensure ports **15672** and **5672** are open in Windows Firewall.

---

## 📱 Mobile App Setup

* Install the app via Android Studio or APK.
* Set:

  * RabbitMQ Server IP
  * Port: `5672`
  * Username: `test`
* Select sensors to stream.
* Check `sendDataService.java` for credential configs.

---

## ✅ Testing

* Start RabbitMQ and the Java consumer
* Launch the app and start data transmission
* Monitor logs and RabbitMQ UI (`Queues`, `Connections` tabs)

---

## 🤝 Contributing

Contributions are welcome!
Feel free to fork, submit PRs, or report issues.

