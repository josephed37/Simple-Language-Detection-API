# Simple Language Detection App

## Overview
This is a simple **language detection API** built using **FastAPI** and **Scikit-Learn**. The model predicts the language of a given text string. The API is containerized using **Docker** to ensure easy deployment and scalability.
This is inspired by [https://github.com/basil-b2s/Language-Detector](https://github.com/basil-b2s/Language-Detector)

## Features
- Predicts the language of a given text input.
- Uses a trained **Scikit-Learn** model for classification.
- Provides a REST API with **FastAPI**.
- Dockerized for easy deployment.
- Lightweight and fast inference.

## Tech Stack
- **Python 3.9**
- **FastAPI** (for API development)
- **Scikit-Learn** (for machine learning model)
- **Uvicorn** (for running the FastAPI app)
- **Docker** (for containerization)

## Installation and Setup
### 1. Clone the Repository
```sh
git clone https://github.com/josephed37/Simple-Language-Detection-App.git
cd Simple-Language-Detection-App
```

### 2. Create a Virtual Environment (Optional but Recommended)
```sh
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```


## Docker Setup
### 1. Build the Docker Image
```sh
docker build -t language-detection-app .
```

### 2. Run the Docker Container
```sh
docker run -p 80:80 language-detection-app
```

Your API should now be running inside a Docker container and accessible at: [http://localhost:80](http://localhost:80)

## API Endpoints
### 1. Health Check
```http
GET /
```
**Response:**
```json
{
  "health_check": "OK",
  "model_version": "0.1.0"
}
```

### 2. Predict Language
```http
POST /predict
```
#### Request Body (JSON):
```json
{
  "text": "Bonjour tout le monde"
}
```
#### Response:
```json
{
  "language": "French"
}
```

## Deploying to Cloud Platforms
You can deploy this app to cloud platforms like:
- **AWS EC2**: [Deploy FastAPI with Docker on AWS](https://towardsdatascience.com/deploy-fastapi-on-aws-ec2-with-docker-9cf78a6c7198)
- **Heroku**: [Deploy FastAPI with Docker on Heroku](https://testdriven.io/blog/fastapi-docker-uvicorn/)
- **Google Cloud Run**: [Deploy FastAPI on Google Cloud](https://cloud.google.com/run/docs/quickstarts/build-and-deploy/deploy-python-service)

## Additional Learning Resources
- **FastAPI Documentation**: [https://fastapi.tiangolo.com/](https://fastapi.tiangolo.com/)
- **Docker & FastAPI Integration**: [https://fastapi.tiangolo.com/deployment/docker/](https://fastapi.tiangolo.com/deployment/docker/)
- **Scikit-Learn Documentation**: [https://scikit-learn.org/stable/](https://scikit-learn.org/stable/)

## Contributing
If you'd like to contribute to this project, feel free to fork the repo, create a new branch, and submit a pull request.

## License
This project is licensed under the **MIT License**.

---

Now you're all set to use the **Simple Language Detection App** with FastAPI and Docker! 🚀

