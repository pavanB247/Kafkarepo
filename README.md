Perfect 👍 I’ll give you the **entire README.md** content in one single block, so you can just **copy once** and paste it directly into your GitHub README file.

Here’s the complete document:

````markdown
# ⚡ Kafka Producer Example

This repository demonstrates how to set up and run a **Kafka Producer** locally using both **Apache Kafka** and **Confluent Kafka Community Edition**.  

---

## 🚀 Open Source Kafka (Apache) Setup

### 🔹 1. **Start Zookeeper Server**
```sh
sh bin/zookeeper-server-start.sh config/zookeeper.properties
````

### 🔹 2. **Start Kafka Server / Broker**

```sh
sh bin/kafka-server-start.sh config/server.properties
```

### 🔹 3. **Create a Topic**

```sh
sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --topic NewTopic --partitions 3 --replication-factor 1
```

### 🔹 4. **List All Topics**

```sh
sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --list
```

### 🔹 5. **Describe a Topic**

```sh
sh bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic NewTopic
```

### 🔹 6. **Produce Messages**

```sh
sh bin/kafka-console-producer.sh --broker-list localhost:9092 --topic NewTopic
```

### 🔹 7. **Consume Messages**

```sh
sh bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic NewTopic --from-beginning
```

---

## 🟣 Confluent Kafka Community Edition Setup

### 🔹 1. **Start Zookeeper Server**

```sh
bin/zookeeper-server-start etc/kafka/zookeeper.properties
```

### 🔹 2. **Start Kafka Server / Broker**

```sh
bin/kafka-server-start etc/kafka/server.properties
```

### 🔹 3. **Create a Topic**

```sh
bin/kafka-topics --bootstrap-server localhost:9092 --create --topic NewTopic1 --partitions 3 --replication-factor 1
```

### 🔹 4. **List All Topics**

```sh
bin/kafka-topics --bootstrap-server localhost:9092 --list
```

### 🔹 5. **Describe a Topic**

```sh
bin/kafka-topics --bootstrap-server localhost:9092 --describe --topic NewTopic1
```

### 🔹 6. **Produce Messages**

```sh
bin/kafka-console-producer --broker-list localhost:9092 --topic NewTopic1
```

### 🔹 7. **Consume Messages**

```sh
bin/kafka-console-consumer --bootstrap-server localhost:9092 --topic NewTopic1 --from-beginning
```

---

## 📂 Sending a CSV File to Kafka

You can also send **CSV file data** directly to a Kafka topic:

```sh
bin/kafka-console-producer --broker-list localhost:9092 --topic NewTopic1 < bin/customers.csv
```

---
