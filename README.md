# 🎯 Student Performance Measure Model

This project predicts student performance using machine learning models and demonstrates a complete **MLOps workflow** including data preprocessing, model training, pipeline creation, experiment tracking, and containerization with Docker.

---

## 🚀 Project Overview
The goal of this project is to analyze student data and predict academic performance based on various factors like study hours, attendance, parental education, and test preparation.  
The project integrates an **end-to-end ML lifecycle** — from preprocessing and model training to experiment tracking and deployment using **MLflow** and **Docker**.

---

## 🧠 Key Features
- Built and compared multiple ML models (CatBoost, XGBoost, Random Forest, etc.)
- Implemented **data preprocessing and feature engineering pipelines**
- Created a **modular and reusable ML pipeline** using `Scikit-learn`
- Tracked model experiments, parameters, and metrics with **MLflow**
- Containerized the workflow using **Docker** for consistent and reproducible deployments

---

## 🧩 Tech Stack
- **Languages & Libraries:** Python, Pandas, NumPy, Scikit-learn, CatBoost, XGBoost  
- **MLOps Tools:** MLflow, Docker  
- **Others:** Matplotlib, Seaborn (for visualization)

---

## ⚙️ Workflow
1. **Data Preprocessing:**  
   - Handled missing values, outliers, and categorical encoding  
   - Scaled features using `StandardScaler`  

2. **Model Training:**  
   - Trained multiple boosting models (CatBoost, XGBoost, LightGBM)  
   - Compared model performances using cross-validation  

3. **Pipeline Creation:**  
   - Built reusable ML pipelines integrating preprocessing and model training  
   - Automated training workflow for scalability  

4. **Experiment Tracking:**  
   - Used **MLflow** to log parameters, metrics, and artifacts  
   - Visualized model performance and versioning  

5. **Containerization:**  
   - Created a **Dockerfile** to package the model and dependencies  
   - Built and ran Docker images for consistent deployment across systems  

---

## 🐳 Docker Setup

### 1. Build the Docker Image
```bash
docker build -t student-performance-mlops .
```

### 2. Run the Docker Container
```bash
docker run -p 5000:5000 student-performance-mlops
```

---

## ☸️ Kubernetes Setup

### 1. Deploy to Kubernetes
Apply the deployment and service manifests:
```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

### 2. Verify Resources
```bash
kubectl get pods
kubectl get services
```

### 3. Access the Application
If you are using Minikube:
```bash
minikube service ml-project-service
```
Otherwise, check the service status to find the external IP:
```bash
kubectl get service ml-project-service
```

---

## 📊 Results

Achieved high accuracy and robustness with CatBoost

Improved model interpretability using feature importance visualization

Fully automated training pipeline ready for scalable deployment

## 💡 Future Improvements

Integrate CI/CD using GitHub Actions

Add automated model monitoring and retraining

Deploy model as a REST API or Streamlit web app


---

⭐ If you like this project, give it a star on GitHub!

---
```bash
# Clean up
docker stop $(docker ps -q --filter ancestor=student-performance-mlops)
```
