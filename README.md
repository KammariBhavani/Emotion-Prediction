# Emotion-Prediction

📌 Overview

This project builds an intelligent system that analyzes user behavior and emotional signals from real-world data. It predicts the user’s emotional state and intensity, and provides meaningful action recommendations along with the right timing.

The focus is on combining machine learning with decision-making to create a practical, human-centered solution.

🎯 Objectives

Understand user emotions from text and contextual data

Predict emotional state (classification)

Predict emotional intensity (regression)

Recommend actions and timing using a decision engine

📂 Dataset Description
arvyax_test_inputs_120

Includes the following features:

journal_text – User’s written thoughts

sleep_hours, stress_level, energy_level – Personal indicators

time_of_day, ambience_type – Contextual information

face_emotion_hint – Additional emotion signal

reflection_quality – Clarity of expression

emotional_state – Target label

intensity – Target value

Sample_arvyax_reflective_dataset

Same structure as arvyax_test_inputs_120 data but without:

emotional_state

intensity

⚙️ Project Workflow
Input Data
   ↓
Text Cleaning & Processing
   ↓
Feature Engineering (TF-IDF + Categorical + Numerical)
   ↓
Emotion Classification Model
   ↓
Intensity Prediction Model
   ↓
Decision Engine (Rule-Based)
   ↓
Final Output (Emotion + Intensity + Action + Time)

Data Preprocessing

Converted text to lowercase and removed special characters

Applied TF-IDF vectorization on journal text

One-hot encoded categorical features

Combined all features using hstack

🤖 Models Used

Emotion Prediction

Model: Random Forest Classifier

Output: Predicted emotional state

Intensity Prediction

Model: Random Forest Regressor

Output: Predicted intensity score

🧠 Decision Engine

A rule-based system designed to provide actionable recommendations based on predictions and user context.

Example Logic:

High stress + high intensity → Immediate action required

Low sleep → Recommend rest

Sad/anxious → Suggest calming or social activities

Happy → Encourage continuation of current activity

This component is key to making the system practical and useful.

📤 Output Format

The final output file (final_output.csv) contains:

id

predicted_emotion

predicted_intensity

recommended_action

recommended_time

🚀 How to Run

Install required libraries:

pip install pandas numpy scikit-learn scipy

Place dataset files in the project folder

Run the script:

python EmotionPrediction.ipynb

Output will be generated as:

final_output.csv

📁 Project Structure
Emotion-Prediction/
│
├── data/
│   ├── arvyax_test_inputs_120.xlsx
│   ├── Sample_arvyax_reflective_dataset.csv
│
├── EmotionPrediction.ipynb
├── final_output.csv
├── README.md


💡 Key Highlights

Combines NLP and structured data
Handles real-world messy inputs
Focuses on decision-making, not just prediction


Future Improvements

Use advanced NLP techniques (word embeddings, transformers)
Improve decision engine with learning-based approaches
Add personalization for individual users
Deploy as a web application

📌 Conclusion

This project demonstrates how machine learning can be extended beyond prediction to build systems that provide meaningful, real-world decisions and recommendations.
