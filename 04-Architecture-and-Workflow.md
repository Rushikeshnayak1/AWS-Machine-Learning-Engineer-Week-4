# Conceptual Architecture and Workflow Diagrams

These are **illustrative diagrams based on slide topics**, not deployed or tested AWS architectures. GitHub renders Mermaid diagrams in Markdown.

## Streaming analytics workflow
```mermaid
flowchart LR
  A[Incoming events] --> B[Streaming source]
  B --> C[Managed Apache Flink / analytics]
  C --> D[AWS Lambda processing]
  D --> E[Destination: S3 or DynamoDB]
```

## Amazon MSK Kafka model
```mermaid
flowchart LR
  P[Kafka producer] --> T[MSK topic / partitions]
  T --> C[Kafka consumer]
```

## Amazon EMR cluster roles
```mermaid
flowchart TB
  M[Master node: coordination] --> C[Core nodes: compute + HDFS]
  M --> T[Task nodes: compute only]
  S[Amazon S3 input / output] <--> C
```

## Spark and feature engineering workflow
```mermaid
flowchart LR
  D[Input dataset] --> S[Spark distributed processing]
  S --> F[Feature selection and transformation]
  F --> M[ML model inputs]
```
