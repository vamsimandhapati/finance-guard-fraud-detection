# FinanceGuard Fraud Detection

Real-time financial fraud detection microservices with Kafka event streaming, ML anomaly detection, Spring Boot, React dashboard, and AWS deployment.

[![Java 17](https://img.shields.io/badge/Java-17-ED8B00?style=flat&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Spring Boot 3.2](https://img.shields.io/badge/Spring--Boot-3.2-6DB33F?style=flat&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Apache Kafka](https://img.shields.io/badge/Apache--Kafka-3.6-231F20?style=flat&logo=apache-kafka&logoColor=white)](https://kafka.apache.org/)
[![AWS](https://img.shields.io/badge/AWS-Deployed-FF9900?style=flat&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)

## Overview

FinanceGuard is a high-throughput fraud detection system designed for modern banking. It uses a microservices architecture to ingest transaction streams via Kafka, process them through a machine learning model for anomaly detection, and provide real-time alerts to a React-based security dashboard.

## Key Features

- **Real-time Ingestion**: Distributed transaction logging using Apache Kafka with high-availability configuration.
- **Anomaly Detection**: Python-based ML service integrated via REST/gRPC to score transactions for fraud probability.
- **Event-Driven Architecture**: Decoupled microservices using Spring Cloud Stream.
- **Security Dashboard**: Live monitoring of "High Risk" transactions with geographic mapping and clinician alerts.
- **Audit Logging**: Immutable transaction history stored in PostgreSQL with historical reporting via ELK Stack.

## Tech Stack

- **Backend**: Spring Boot 3.2, Java 17, Spring Security (OAuth2).
- **Data Streaming**: Apache Kafka, Kafka Streams.
- **Machine Learning**: Scikit-learn (Isolation Forest), Python FastAPI.
- **Frontend**: React.js, Socket.io (for real-time updates), Material UI.
- **Infrastructure**: AWS MSK (Kafka), RDS, Elastic Beanstalk, Docker.

## Project Structure

```text
├── transaction-service/   # Java/Spring Boot ingestion service
├── fraud-ml-engine/       # Python/FastAPI anomaly detection service
├── security-dashboard/    # React live monitoring app
├── infrastructure/        # Kubernetes (EKS) and Helm charts
└── kafka-config/          # Topic configurations and schemas
```

## License

MIT License. See [LICENSE](LICENSE) for details.
