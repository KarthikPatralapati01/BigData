# 🌟 Yelp Sentiment Analysis on Google Cloud Platform

**Real-time + Batch ML pipeline** for extracting actionable insights from Yelp reviews using fully managed GCP services and scalable Apache Spark processing.

> 🚀 A modern ML engineering pipeline built for speed, scale, and continuous learning.

---

## 🧠 Project Highlights

- ⚡ **Real-Time Streaming** from Yelp API → Google Cloud Pub/Sub  
- 🔎 **Sentiment Classification** using PySpark + Spark MLlib (LogReg, SVM, Naive Bayes)  
- 🧺 **Batch Model Training** on historical data via Cloud Storage + Dataproc  
- 📊 **Insightful Visualizations** using BigQuery + Looker Studio  
- 🔁 **Auto-Retraining** for continued model relevance over time  

---

## ⚙️ Tech Stack

| Layer             | Tools/Services |
|------------------|----------------|
| **Modeling**      | PySpark, Spark MLlib, Logistic Regression, Naive Bayes, SVM |
| **Streaming**     | Google Cloud Pub/Sub |
| **Data Warehouse**| BigQuery |
| **Processing**    | Dataproc (Spark on GCP) |
| **Storage**       | Cloud Storage |
| **Deployment**    | Cloud Functions |
| **Visualization** | Looker Studio (formerly Data Studio) |

---

## 🧩 Pipeline Architecture
🗃️ Data Pipeline Stages
1. 📥 Ingestion
Real-time Yelp reviews streamed to Pub/Sub topic.

Data lands in BigQuery (raw layer) for staging.

2. 🔄 Streaming Pipeline
BigQuery triggers a Dataproc PySpark job for:

Text cleaning

Tokenization

TF-IDF vectorization

Inference using pre-trained models

3. 📦 Batch Training Pipeline
Historical data stored in Cloud Storage

Trained using Spark MLlib on Dataproc with:

Logistic Regression

Support Vector Machine (SVM)

Naive Bayes classifiers

Best-performing model exported and deployed to Cloud Functions

4. 📊 Visualization
Predictions and trends stored in BigQuery

Dashboards created using Looker Studio

Sentiment by category

Sentiment trend over time

Review volume heatmaps

5. 🔁 Retraining (Optional)
Periodic job (Airflow or manual) to retrain models with new data

🧪 Experiments
Model	Accuracy	AUC Score	Notes
Logistic Regression	84.3%	0.88	Fast and consistent
Naive Bayes	80.5%	0.84	Performs well on sparse text
SVM	85.1%	0.89	Slightly higher accuracy, slower inference
📎 Key Features
✅ Scalable to millions of reviews using Spark on Dataproc

✅ Built entirely with serverless and managed GCP services

✅ Supports both real-time prediction and batch retraining

✅ End-to-end automation ready with triggers and functions

✅ Visual insights easily shareable with business teams

🧠 Future Enhancements
 Add BERT/Transformer-based sentiment model for improved accuracy

 AutoML integration for Auto retraining and hyperparameter tuning

 Alerting on sentiment shifts via Cloud Monitoring

