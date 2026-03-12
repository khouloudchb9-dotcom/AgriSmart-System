# Project Structure – AgriSmart

AgriSmart est divisé en deux parties principales :

* **Frontend** : Interface utilisateur développée avec React
* **Backend** : API et logique serveur développées avec FastAPI

---

# Structure générale du projet

```
AgriSmart/
│
├── frontend/                       # Application React
│
│   ├── public/
│   │   └── index.html
│   │
│   ├── src/
│   │
│   │   ├── assets/                 # Images, icônes, styles
│   │
│   │   ├── components/             # Composants réutilisables
│   │   │   ├── Navbar.jsx
│   │   │   ├── Footer.jsx
│   │   │   └── ProductCard.jsx
│   │
│   │   ├── pages/                  # Pages principales
│   │   │   ├── Home.jsx
│   │   │   ├── Marketplace.jsx
│   │   │   ├── ProductDetails.jsx
│   │   │   ├── Experts.jsx
│   │   │   ├── Chatbot.jsx
│   │   │   ├── Login.jsx
│   │   │   └── Register.jsx
│   │
│   │   ├── dashboards/             # Dashboards selon le rôle
│   │   │   ├── BuyerDashboard.jsx
│   │   │   ├── SellerDashboard.jsx
│   │   │   └── ExpertDashboard.jsx
│   │
│   │   ├── services/               # Communication avec l'API backend
│   │   │   └── api.js
│   │
│   │   ├── App.jsx
│   │   └── main.jsx
│
│   └── package.json
│
│
├── backend/                        # Backend FastAPI
│
│   ├── app/
│   │
│   │   ├── main.py                 # Point d'entrée de l'API
│   │
│   │   ├── core/                   # Configuration générale
│   │   │   ├── config.py
│   │   │   └── security.py
│   │
│   │   ├── models/                 # Modèles de base de données
│   │   │   ├── user.py
│   │   │   ├── product.py
│   │   │   ├── order.py
│   │   │   ├── expert.py
│   │   │   ├── consultation.py
│   │   │   └── review.py
│   │
│   │   ├── schemas/                # Schémas Pydantic
│   │   │   ├── user_schema.py
│   │   │   ├── product_schema.py
│   │   │   ├── order_schema.py
│   │   │   ├── consultation_schema.py
│   │   │   └── review_schema.py
│   │
│   │   ├── routes/                 # Routes API
│   │   │   ├── auth_routes.py
│   │   │   ├── product_routes.py
│   │   │   ├── order_routes.py
│   │   │   ├── expert_routes.py
│   │   │   ├── consultation_routes.py
│   │   │   ├── review_routes.py
│   │   │   └── chatbot_routes.py
│   │
│   │   ├── services/               # Logique métier
│   │   │   ├── product_service.py
│   │   │   ├── consultation_service.py
│   │   │   └── recommendation_service.py
│   │
│   │   ├── database/
│   │   │   ├── connection.py
│   │   │   └── base.py
│   │
│   │   └── utils/
│   │       └── location_utils.py
│
│   └── requirements.txt
│
│
└── README.md                       # Documentation du projet
```

---

# Description des parties

## Frontend (React)

Le frontend gère l’interface utilisateur de la plateforme AgriSmart.

Il permet :

* l’affichage du marché agricole
* la recherche de produits
* la consultation des experts et jardiniers
* l’accès aux dashboards (acheteur, vendeur, expert)
* l’utilisation du chatbot intelligent
* la communication avec l’API backend

---

## Backend (FastAPI)

Le backend gère la logique de l’application et les services API.

Il permet :

* la gestion des utilisateurs
* la gestion des produits agricoles
* la gestion des commandes
* la gestion des experts et jardiniers
* la gestion des consultations
* la gestion des avis et évaluations
* l’intégration du chatbot IA
* les recommandations basées sur la localisation

---

# Technologies utilisées

## Frontend

* React
* Axios
* CSS / Tailwind

## Backend

* FastAPI
* Pydantic
* SQLAlchemy
* PostgreSQL

## Intelligence Artificielle

* Chatbot agricole
* Recommandation d’experts et produits
