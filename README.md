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

# Project Architecture & Workflow
The user inputs symptoms on the web page and submits the form.

The Flask app receives the symptoms (request.form).

The symptoms are converted into a binary feature vector using a pre-defined symptoms_dict.

This vector is fed into the pre-trained svc.pkl model.

The model returns a predicted disease number, which is mapped to a disease name using diseases_list.

The helper function helper() queries all CSV datasets for information related to the predicted disease.

The retrieved data (description, precautions, etc.) is passed to the HTML template.

The template is rendered and displayed to the user with the results.

# Installation & Local Setup
Prerequisites:

Python 3.8+

pip (Python package manager)
