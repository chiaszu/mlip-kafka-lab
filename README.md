# My Kafka Learning Project

This repository contains my implementation of Apache Kafka producer-consumer patterns and streaming data processing.

## 🎯 Project Overview

Started as a class lab, now extended as a personal exploration of Kafka's capabilities for real-time data streaming and processing.

## 📋 Completed Features

### Core Kafka Implementation
- ✅ **SSH Tunnel Setup**: Secure connection to remote Kafka server
- ✅ **Producer Mode**: Streams weather data for multiple cities
- ✅ **Consumer Mode**: Reads and processes messages with offset management
- ✅ **CLI Tools**: Using `kcat` for topic management and monitoring

### Data Pipeline
- **Cities**: Pittsburgh, New York, San Francisco
- **Data Format**: JSON with city, timestamp, and temperature
- **Offset Strategy**: `earliest` for complete message history

## 🛠️ Tech Stack

- **Apache Kafka**: Distributed streaming platform
- **Python**: kafka-python library for producers/consumers
- **kcat**: Command-line Kafka toolkit
- **Jupyter Notebook**: Interactive development environment

## 🚀 Getting Started

### Prerequisites
```bash
# Install kcat
brew install kcat  # macOS
apt-get install kcat  # Ubuntu
```

### Setup SSH Tunnel
```bash
ssh -L 9092:localhost:9092 user@remote-server -NTf
```

### Run the Notebook
Open `KafkaDemo.ipynb` and execute the cells to see the producer-consumer pattern in action.

## 📊 Key Learnings

### Kafka Concepts Mastered
- **Topics & Partitions**: Message organization and distribution
- **Offsets**: Message ordering and consumer resume capability  
- **Consumer Groups**: Load balancing and fault tolerance
- **auto_offset_reset**: Different strategies for new consumers

### CLI Commands
```bash
# List all topics
kcat -b localhost:9092 -L

# Consume messages with offset info
kcat -b localhost:9092 -t my-topic -C -c 5 -o beginning -f 'Offset: %o, Message: %s\n'
```

## 🔮 Future Extensions

Planning to build a **Movie Recommendation Pipeline** using existing movielog streams:
- Real-time viewing pattern analysis
- Collaborative filtering recommendations  
- Dashboard for recommendation insights

## 📚 Resources

- [Apache Kafka Documentation](https://kafka.apache.org/documentation/)
- [kafka-python Library](https://kafka-python.readthedocs.io/)
- [kcat Usage Guide](https://docs.confluent.io/platform/current/app-development/kafkacat-usage.html)

---

*This project demonstrates practical understanding of distributed streaming systems and real-time data processing.*