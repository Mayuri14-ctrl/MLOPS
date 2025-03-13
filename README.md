# MLOPS
## Real-Time Fraud Detection System
🔷 Phase 1: Data Streaming & Feature Engineering
Goal: Set up a real-time data pipeline to process transaction data.
✅ Step 1: Simulate a stream of transactions (Kafka Producer) (Pub /sub on GCP)
✅ Step 2: Preprocess data in real-time with Flink (e.g., feature aggregation, encoding) (Dataflow on GCP)
✅ Step 3: Store processed features in Redis for fast retrieval
✅ Step 4:Store Data in BigQuery for Monitoring: Create a BigQuery dataset (fraud_detection)
Set up a Dataflow job to write fraud logs to BigQuery

🔷 Phase 2: Model Development & Optimization
Goal: Train a fraud detection model that balances accuracy and speed.
✅ Step 4: Train XGBoost/LightGBM on a fraud dataset (e.g., Kaggle Credit Card Fraud)
✅ Step 5: Convert model for efficient inference (ONNX/TensorRT)
✅ Step 6: Deploy model using Triton Inference Server

🔷 Phase 3: Real-Time Inference & Monitoring
Goal: Deploy the system with low latency inference and monitoring.
✅ Step 7: Create a FastAPI service to call the fraud detection model
✅ Step 8: Integrate Kafka Consumer for real-time inference
✅ Step 9: Set up Prometheus + Grafana for monitoring

We need: (1) a data ingestion layer using Kafka/PubSub for real-time data or Airflow for batch, (2) a feature store like Feast for online and offline feature consistency, (3) a model training pipeline with distributed training using Vertex AI/Kubeflow, (4) model serving via TensorFlow Serving, and (5) monitoring with Prometheus to detect drift. Given my background in ML model deployment and inference optimization, I’d focus on ensuring model retraining integrates seamlessly with the pipeline.

