# AWS Study Notes

## Part 1 – Streaming Analytics and Amazon MSK
- **Streaming analytics:** Process events as they arrive; SQL-style aggregations can count records by key and reference data can enrich events.
- **AWS Lambda:** Can post-process analytics output and send it to other AWS destinations.
- **Managed Service for Apache Flink:** Managed stream processing for continuous ETL and analytics; the slides discuss KPUs as capacity units.
- **Anomaly detection:** `RANDOM_CUT_FOREST` is introduced for identifying unusual numeric stream values.
- **Amazon MSK:** Managed Apache Kafka infrastructure with brokers, topics, producers, and consumers; slides cover VPC deployment, multiple AZs, encryption, IAM/Kafka authentication, CloudWatch, MSK Connect, and Serverless.

## Part 2 – Amazon EMR
- **EMR:** Managed big-data processing using frameworks such as Hadoop and Spark.
- **Node roles:** Master coordinates; core processes and stores HDFS data; task processes without HDFS storage.
- **Cluster operation:** Transient or long-running; capacity and instance purchasing choices influence cost.
- **Storage:** HDFS, EMRFS/S3, local file system, and EBS.
- **Integrations:** EC2, VPC, S3, CloudWatch, IAM, CloudTrail.
- **EMR Serverless:** Submit jobs without managing a conventional cluster; worker configuration and execution permissions still matter.
- **EMR on EKS:** The final slide introduces running Spark jobs with Amazon EKS.

## Part 3 – Apache Spark and Feature Engineering
- **Hadoop:** HDFS for storage, YARN for resource management, MapReduce for processing.
- **Spark architecture:** Driver coordinates tasks; cluster manager allocates resources; executors perform parallel work and may cache data.
- **Spark libraries:** Spark SQL, Structured Streaming, MLlib, GraphX; MLlib examples include classification, clustering, regression and recommendations.
- **Notebooks:** Zeppelin and EMR notebooks support interactive work and visualizations.
- **Feature engineering:** Choose, transform, and create informative inputs; handle missing values and use domain knowledge.
- **Dimensionality:** Too many features can increase complexity; feature selection and reduction may help.
- **TF-IDF and n-grams:** Represent word importance and sequences for text processing.

**Note:** These notes summarize the supplied slides, not an independent validation of current AWS service names or capabilities.
