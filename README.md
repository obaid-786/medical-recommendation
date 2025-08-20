# MediRec: AI-Powered Medical Symptom Analysis and Recommendation System
A Flask-based web application that uses a Machine Learning model to predict potential diseases from user-reported symptoms and provides a comprehensive care plan including descriptions, precautions, medications, diets, and workouts.

# Overview
MediRec is an intelligent web application designed to act as a preliminary medical advisory tool. Users can input a list of symptoms they are experiencing. The application leverages a pre-trained Support Vector Classifier (SVC) model to predict the most likely disease. Based on the prediction, it then fetches and displays a detailed care plan from its knowledge base, which includes:

A description of the disease.

Important precautions to take.

Common medications used (Note: Always consult a real doctor).

Recommended dietary plans.

Suggested workout routines.
# Features
Symptom Analysis: Accepts multiple symptoms as comma-separated input.

AI-Powered Prediction: Utilizes a robust SVC model for accurate disease prediction.

Comprehensive Care Plan: Provides a holistic view of recommended actions post-prediction.

Responsive Web Interface: Built with HTML/CSS (and likely Bootstrap/Jinja2 templates) for ease of use.

Informational Pages: Includes About, Contact, Developer, and Blog pages for a complete user experience.

# Tech Stack
Backend Framework: Flask (Python)

Machine Learning:

scikit-learn (Support Vector Classifier - SVC)

pandas for data handling

numpy for numerical operations

pickle for model serialization & loading

Frontend: HTML5, CSS3, JavaScript (with Jinja2 templating)

Data Storage: Flat-file databases (CSV files acting as a knowledge base)


graph LR
A[User] -->|Enters Symptoms| B(Flask Web App)
B -->|Preprocesses Input| C(SVC Model)
C -->|Returns Prediction| B
B -->|Queries Knowledge Base CSVs| D[(CSV Datasets)]
D -->|Returns Description, Precautions, etc.| B
B -->|Renders Results| A
