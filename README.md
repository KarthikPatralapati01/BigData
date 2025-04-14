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

```mermaid
graph TD
  A[Yelp API] -->|Stream JSON| B(Pub/Sub)
  B --> C[BigQuery (Raw Layer)]
  C --> D{Trigger}
  D -->|Batch/Trigger| E[Dataproc PySpark Job]
  E --> F[Model Training + Predictions]
  F --> G[BigQuery (Processed)]
  F --> H[Cloud Functions (Model API)]
  G --> I[Looker Studio Dashboard]
