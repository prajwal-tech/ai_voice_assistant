# ai_voice_assistant

# AI Voice Assistant

## Description
A simple AI Voice Assistant API built using FastAPI. It processes text input (simulating voice), recognizes basic intents, stores interactions in MongoDB, and is containerized using Docker.

## Features
- FastAPI-based backend
- Basic intent recognition (hello, bye, help)
- MongoDB integration for storing interactions
- Dockerized for easy deployment
- Logging for API requests/responses

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd ai_voice_assistant
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run MongoDB (Optional, if storing chats)
Ensure MongoDB is running locally or use a cloud instance.
```bash
docker run -d -p 27017:27017 --name mongo mongo
```

### 4. Start the FastAPI Server
```bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

### 5. Docker Build & Run
```bash
docker build -t ai_voice_assistant .
docker run -p 8000:8000 ai_voice_assistant
```

### 6. API Endpoints
- `GET /` - Check if the server is running
- `POST /chat` - Send text input and get a response
- `GET /chats` - Retrieve stored chat history (if MongoDB is used)

### 7. Deployment (Bonus)
To push to DockerHub:
```bash
docker tag ai_voice_assistant <your-dockerhub-username>/ai_voice_assistant
docker push <your-dockerhub-username>/ai_voice_assistant
```

For Kubernetes deployment, create a Kubernetes YAML file and apply it:
```bash
kubectl apply -f deployment.yaml
```

## Video Demo
(Insert link to demo video)

## License
MIT
