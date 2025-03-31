## Todo App 📔

- React JS
- FastAPI
- Sqlalchemy
- Tailwind CSS

![Todo gif](https://user-images.githubusercontent.com/64283478/204075904-bfb3d555-b736-4501-b30b-70c256d5c75a.gif)

# Buddywise CI/CD Project

##  Project Overview
Buddywise is a web application consisting of a frontend (React) and a backend (Python). This project includes CI/CD automation using GitHub Actions and Kubernetes deployment.

## 📂 Folder Structure
```
BUDDYWISE/
│── .github/workflows/     # GitHub Actions CI/CD workflows
│── backend/               # Python backend source code
│── frontend/              # React frontend source code
│── kubernetes/                   # Kubernetes manifests
│   ├── development-deployment.yaml    # Deployment configurations
│   ├── prod-deployment.yaml       # Service configurations
│── docker-compose.yml     # Local development Docker setup
│── README.md              # Project documentation
```

## 🛠️ Setup & Installation
### Prerequisites
- [Docker](https://www.docker.com/)
- [Kubernetes (kubectl)](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Helm](https://helm.sh/docs/intro/install/)
- Python 3.9 & Node.js

### Clone the Repository
```sh
git clone https://github.com/your-username/buddywise.git
cd buddywise
```

### Install Backend Dependencies
```sh
cd backend
pip install -r requirements.txt
```

### Install Frontend Dependencies
```sh
cd frontend
npm install
```

## 🚢 Running the Application
### Using Docker
```sh
docker-compose up --build
```

### Running Locally (Without Docker)
#### Start Backend
```sh
cd backend
python main.py
```

#### Start Frontend
```sh
cd frontend
npm start
```

## 🤖 CI/CD Pipeline (GitHub Actions)
This project uses GitHub Actions to:
1. Run tests for frontend & backend
2. Build Docker images
3. Push images to Docker Hub
4. Deploy to Kubernetes

# Deploying to Kubernetes
# Apply Kubernetes Manifests
```sh
kubectl apply -f k8s/
```

### Check Deployment Status
```sh
kubectl get pods
```

### Expose the Application
```sh
kubectl port-forward svc/buddywise-service 8080:80
```
Then visit: `http://localhost:8080`
