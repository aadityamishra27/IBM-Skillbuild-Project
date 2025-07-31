# IBM-Skillbuild-Project
This project uses IBM Watsonx.ai to build a machine learning model that detects and classifies power system faults. The deployed Random Forest Classifier predicts specific fault types to enable rapid identification, aiming to improve overall grid stability and reliability.

# Power System Fault Detection and Classification using Machine Learning
This project demonstrates the use of machine learning, specifically through IBM's cloud services, to automatically detect and classify various types of faults in a power distribution system. The goal is to create a reliable system that can quickly identify faults, helping to improve the stability and reliability of the power grid.

📋 Table of Contents
Problem Statement

Dataset

Technologies Used

Methodology

Results

Deployment

How to Reproduce

🎯 Problem Statement
The core challenge was to design a machine learning model capable of distinguishing between normal operating conditions and various fault conditions in a power system. Using electrical measurement data, the model needed to accurately classify different fault types, such as line-to-ground, line-to-line, or three-phase faults. The primary objective is to enable rapid and accurate fault identification, a critical task for maintaining power grid integrity.

💾 Dataset
The model was trained using the Power System Faults Dataset available on Kaggle. This dataset contains thousands of records of electrical measurements (current and voltage phasors) under various normal and faulty conditions.

Source: Kaggle Power System Faults Dataset

💻 Technologies Used
This project was developed entirely on the IBM Cloud platform, leveraging its powerful AI and ML services.

Cloud Platform: IBM Cloud

AI/ML Service: IBM Watsonx.ai Studio

Key Feature: AutoAI Experiment for automated model building, training, and optimization.

Underlying Libraries: The AutoAI service managed the use of core Python libraries, including:

Scikit-learn (for the Random Forest Classifier)

Pandas (for data manipulation)

ibm-watson-machine-learning (for interacting with the IBM Cloud services)

⚙️ Methodology
The project followed a structured workflow from data acquisition to final deployment:

Project Setup: An AI project was initialized within the IBM Watsonx.ai Studio environment.

Data Ingestion: The Power System Faults dataset was uploaded to the project.

Automated Model Building: An AutoAI Experiment was configured with the dataset. The tool automatically performed:

Data Preprocessing

Feature Engineering

Model Selection

Hyperparameter Optimization

Pipeline Evaluation: AutoAI generated and ranked several model pipelines. The Random Forest Classifier pipeline (Pipeline 8) was selected as it achieved the highest accuracy score.

Deployment: The selected pipeline was promoted to a deployment space and deployed as an "Online" web service, making it available for real-time predictions.

✨ Results
The outcome of this project is a fully functional, deployed machine learning model that can successfully classify power system faults.

Functionality: The deployed model (Fault_dp2) provides an interface where a user can input real-time system data (like Power Load, Temperature, Weather Condition, etc.).

Output: Upon receiving input, the model returns a prediction for the specific Fault Type (e.g., "Transformer Failure", "Overheating", "Line Breakage") along with a confidence score for that prediction. This provides an immediate and actionable diagnosis of the system's health.
<img width="1920" height="980" alt="R3" src="https://github.com/user-attachments/assets/c685bb18-66a4-4085-ac6e-22770efc4063" />


<img width="1920" height="1028" alt="R4" src="https://github.com/user-attachments/assets/79624643-f438-48a4-b3c6-550a5eb5738b" />


🚀 Deployment
The final Random Forest model is deployed as a live web service on IBM Cloud. This online deployment provides a REST API endpoint and a user interface for making on-demand predictions. This setup is scalable and allows for easy integration with other applications, such as monitoring dashboards or automated alerting systems.

🔁 How to Reproduce
To reproduce this project, you would need an IBM Cloud account. The high-level steps are as follows:

Sign up for a free IBM Cloud account.

Provision an instance of Watsonx.ai Studio.

Create a new project within the studio.

Download the dataset from the Kaggle link provided above and upload it to your project's assets.

Create a new AutoAI experiment, selecting the uploaded dataset and identifying the "Fault Type" column as the target variable.

Run the experiment and wait for the pipelines to be generated.

Select the top-ranked pipeline and save it as a model.

Promote the saved model to a Deployment Space and create a new "Online" deployment for it.
