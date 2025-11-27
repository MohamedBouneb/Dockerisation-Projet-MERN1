🐳 Dockerisation - Projet MERN
📦 Structure des Containers
Backend (Node.js/Express)
Image: mohamedbouneb/mem-backend

Port: 5000

Base de données: MongoDB

Variables d'environnement:

MONGO_URI: URL de connexion MongoDB

PORT: Port du serveur

Frontend (React)
Image: mohamedbouneb/mem-frontend

Port: 3000

Variables d'environnement:

REACT_APP_API_URL: URL de l'API backend

Base de Données (MongoDB)
Image: mongo:6.0

Port: 27017

Volume: Persistence des données

🚀 Déploiement Local
1. Construction des Images
bash
docker-compose build
2. Lancement des Services
bash
docker-compose up -d
3. Arrêt des Services
bash
docker-compose down
☁️ Publication sur Docker Hub
bash
# Tagging des images
docker tag mern-app-backend mohamedbouneb/mem-backend:latest
docker tag mern-app-frontend mohamedbouneb/mem-frontend:latest

# Publication
docker push mohamedbouneb/mem-backend:latest
docker push mohamedbouneb/mem-frontend:latest
🔗 Accès aux Services
Frontend: http://localhost:3000

Backend: http://localhost:5000

MongoDB: localhost:27017

📁 Structure Docker
text
mern-app/
├── docker-compose.yml
├── backend/
│   ├── Dockerfile
│   └── ...
├── frontend/
│   ├── Dockerfile
│   └── ...
└── README.md
