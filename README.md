# Crack Resistance

Crack Resistance is a password security analysis project designed to identify common password weaknesses and estimate how easily a password could be guessed. It combines rule-based analysis, pattern recognition, and machine learning to provide understandable security feedback.

## Features

- **Password Risk Analysis:** Detects common passwords, dictionary words, and predictable patterns.
- **Pattern Intelligence:** Identifies sequences, repetitions, and common password structures.
- **Personalized Guessability:** Checks for relationships between password components and user-provided personal information.
- **Unrelatedness Analysis:** Evaluates relationships between password fragments and personal terms.
- **Attack Simulation:** Illustrates potential password-guessing approaches.
- **Security Reports:** Provides risk explanations and recommendations for improving password strength.

## Technology Stack

- **Frontend:** React, TypeScript, Vite, Tailwind CSS
- **Backend:** Python, FastAPI
- **Machine Learning:** Scikit-learn, NumPy, Pandas
- **Algorithms:** Logistic Regression, SGDClassifier, character n-gram TF-IDF, and engineered pattern features

## Project Structure

- `frontend/`: User interface, password analysis logic, and browser-side ML inference.
- `backend/app/`: FastAPI application and machine learning training scripts.
- `backend/app/ml/`: Feature extraction, training pipelines, and model implementations.
- `backend/data/ml/`: Training datasets and relationship lexicon.
- `backend/models/`: Directory reserved for trained model artifacts.
- `frontend/public/ml/`: Model files loaded by the frontend.

## Machine Learning

The project includes three ML components:

1. **Pattern Intelligence:** Logistic Regression using engineered password-structure features.
2. **Personalized Relationship Model:** SGDClassifier with character n-gram TF-IDF features to classify relationships between text fragments.
3. **Unrelatedness Model:** SGDClassifier with character n-gram TF-IDF features to classify related and unrelated concept pairs.

The training datasets are generated project fixtures. Their evaluation results should not be interpreted as proof of real-world password-cracking resistance.

## Privacy

The backend currently provides in-memory processing and does not implement persistent password storage. Avoid using real passwords during development or testing. This project is intended for educational and research purposes and is not a guarantee of password security.

## Status

The core analysis modules and ML training pipelines are implemented. Further work includes broader independent dataset evaluation, expanded testing, and improvements to model reliability.

## License

No license has been added yet. Add an appropriate license before permitting reuse or redistribution.
