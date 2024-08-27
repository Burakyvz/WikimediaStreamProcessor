![pipeline drawio](https://github.com/user-attachments/assets/07353284-f6be-4ab0-8a54-c1deaa187f79)

 WikimediaStreamProcessor
A real-time data processing application for Wikimedia change events using Apache Kafka and Java. This project includes components for producing and consuming Kafka streams and is containerized using Docker.


#Wikimedia Stream Processor

## Overview

The Wikimedia Stream Processor is a real-time data processing application designed to capture and process Wikimedia change events using Apache Kafka. The project includes a Kafka producer for streaming data, a consumer for processing the streamed data, and is containerized using Docker for easy setup and deployment.

## Features

- **Kafka Producer**: Streams real-time change events from Wikimedia.
- **Kafka Consumer**: Processes the change events from the Kafka stream.
- **Dockerized Setup**: Simplifies the setup of Kafka environment using Docker.

## Technologies Used

- **Apache Kafka**: For real-time streaming and messaging.
- **Java**: For building the Kafka producer and consumer applications.
- **Docker**: For containerizing and managing the Kafka environment.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Docker installed on your machine.
- Java Development Kit (JDK) installed.
- Apache Kafka binaries downloaded (if running locally without Docker).

## Getting Started

To get a local copy up and running, follow these steps.

### Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/Burakyvz/WikimediaStreamProcessor.git
    cd wikimedia-stream-processor
    ```
2. **Build Docker containers**:

    Ensure Docker is running and execute:

    ```bash
    docker-compose up -d
    ```

3. **Build Java Applications**:

    Navigate to the directory containing your Java files and compile them:

    ```bash
    javac -cp "/path/to/kafka/libs/*" OpenSearchConsumer.java WikimediaChangeHandler.java wikimediaChangesProducer.java WikimediaStreamsApp.java
    ```

4. **Run Producer and Consumer**:

    To run the producer:

    ```bash
    java -cp ".:/path/to/kafka/libs/*" wikimediaChangesProducer
    ```

    To run the consumer:

    ```bash
    java -cp ".:/path/to/kafka/libs/*" OpenSearchConsumer
    ```

## Usage

- **Start Kafka**: Make sure Kafka is running, either via Docker or locally.
- **Run the Producer**: Start the Wikimedia producer to begin streaming data into Kafka.
- **Run the Consumer**: Start the OpenSearch consumer to process data from Kafka.

