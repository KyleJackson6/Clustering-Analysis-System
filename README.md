# Clustering Analysis System

This is a containerized clustering analysis system built with FastAPI, Docker, and OpenAI integration. It allows users to upload datasets, run various clustering algorithms, view evaluation metrics, and interact with an intelligent assistant to explore and understand results.

Repository: https://github.com/KyleJackson6/Clustering-Analysis-System

## Features

- Upload CSV files through the web interface
- Select and run clustering algorithms:
  - KMeans
  - DBSCAN
  - HDBSCAN
  - Agglomerative Clustering
  - Gaussian Mixture Model (GMM)
- Automatically evaluates clustering quality:
  - Silhouette Score
  - Davies-Bouldin Index
- AI assistant integration using OpenAI API for:
  - Metric explanation
  - Result interpretation
  - Clustering insights and recommendations
- FastAPI and Docker-based microservices
- Clean, interactive frontend for experimentation

## Project Structure

```
Clustering-Analysis-System/
├── clustering-agent/         # Core clustering service
├── evaluator-agent/          # Clustering evaluation metrics service
├── frontend/                 # Web interface and OpenAI assistant
├── docker-compose.yml        # Orchestration for all services
├── .env                      # Contains the OpenAI API key (excluded from git)
```

## Requirements

- Docker and Docker Compose installed
- An OpenAI API key (for assistant functionality)

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/KyleJackson6/Clustering-Analysis-System.git
cd Clustering-Analysis-System
```

### 2. Add a `.env` File

Create a file named `.env` in the project root:

```
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

### 3. Start the Application

```bash
docker-compose up --build
```

### 4. Access the Interfaces

- Clustering API Docs: http://localhost:8001/docs
- Frontend Web App: http://localhost:8501

## Notes

- The system adjusts clustering parameters automatically (e.g. reduces K if the dataset is too small).
- Evaluation metrics are shown for supported algorithms.
- Hyperparameter tuning feature is not implemented yet.
- Ensure `.env` is not pushed to GitHub to keep your API key safe.

## License

This project is intended for academic, personal, and demonstration use.