# Real-Time Data Streaming using Kafka, Apache Flink, and Postgres

This project demonstrates a real-time data streaming pipeline using Kafka, Apache Flink, and PostgreSQL. It continuously generates weather data for a city and processes this data through a Kafka-Flink pipeline before storing the results in a PostgreSQL database.

## Overview

The project comprises the following components:
- **Data Generator**: A Python script that generates synthetic weather data and sends it to a Kafka topic.
- **Kafka Producer**: Publishes weather data to a Kafka topic.
- **Apache Flink**: Processes the streaming data from Kafka.
- **Kafka Consumer**: Consumes processed data from Flink and stores it in PostgreSQL.

## Architecture

Data Generator (Python) --> Kafka (Producer) --> Apache Flink --> Kafka (Consumer) --> PostgreSQL


## Prerequisites

Before running the project, ensure you have the following installed:

- Java 8 or above
- Apache Kafka
- Apache Flink
- PostgreSQL
- Python 3.x
- Maven

