# 🚀 OMNI.AFRICA.AI - Digitalisation Intelligente des PME Africaines

## 📋 Description du Projet

OMNI.AFRICA.AI est une plateforme innovante qui utilise l'intelligence artificielle pour accompagner les Petites et Moyennes Entreprises (PME) africaines dans leur transformation numérique. L'application analyse les besoins métier des entreprises et recommande les outils numériques les plus adaptés à leur secteur d'activité.

## 🏗️ Architecture du Projet

Le projet est organisé avec une architecture modulaire et professionnelle :

```
OMNI.AFRICA.AI/
├── frontend/                    # Application Flutter
│   ├── lib/
│   │   ├── core/               # Couche centrale
│   │   │   ├── constants/      # Constantes centralisées
│   │   │   ├── config/         # Configuration
│   │   │   ├── routes/         # Gestion des routes
│   │   │   └── utils/          # Utilitaires
│   │   ├── models/             # Modèles de données
│   │   ├── screens/            # Écrans de l'application
│   │   ├── services/           # Services et API
│   │   ├── theme/              # Thème et styles
│   │   ├── widgets/            # Widgets réutilisables
│   │   └── main.dart           # Point d'entrée
│   ├── assets/                 # Ressources (images, icônes)
│   └── pubspec.yaml            # Dépendances Flutter
├── backend/                     # API Flask/Python
│   ├── config/                 # Configuration
│   ├── routes/                 # Routes API
│   ├── services/               # Services métier
│   ├── database/               # Modèles et migrations
│   ├── utils/                  # Utilitaires
│   ├── middleware/             # Middleware
│   ├── tests/                  # Tests
│   └── app.py                  # Point d'entrée
├── database/                    # Scripts de base de données
├── assets/                      # Ressources partagées
└── docs/                        # Documentation
```

## ✨ Fonctionnalités Principales

### 🎯 Analyse Intelligente des Besoins
- **Saisie Textuelle** : Description détaillée des besoins métier
- **Saisie Vocale** : Reconnaissance vocale multilingue (français, anglais, arabe, swahili, etc.)
- **Analyse IA** : Traitement intelligent avec Gemini AI
- **Recommandations Personnalisées** : Outils adaptés au secteur d'activité

### 🏢 Secteurs d'Activité Supportés
- Agriculture & Élevage
- Commerce & Vente
- Restauration & Hôtellerie
- Transport & Logistique
- Industrie & Production
- Services & Consulting
- Santé & Médical
- Éducation & Formation
- Construction & Immobilier
- Technologie & Digital
- Artisanat & Métiers

### 🔧 Outils Recommandés
- **Gestion de Stock** : FarmLogs, AgriWeb, CropTrak
- **Facturation** : Shopify, WooCommerce, Square
- **CRM** : Salesforce, HubSpot, Pipedrive
- **Comptabilité** : QuickBooks, Wave, Xero
- **Marketing Digital** : Mailchimp, Hootsuite, Buffer
- **E-commerce** : Shopify, Magento, WooCommerce

### 🌍 Support Multilingue
- **Français** (langue principale)
- **Anglais**
- **Arabe**
- **Swahili**
- **Yorùbá**
- **Hausa**
- **Zulu**
- **Xhosa**
- **Portuguais**
- **Espagnol**

### 🔐 Authentification Sécurisée
- **Création de Compte** : Inscription avec validation
- **Connexion** : Authentification JWT
- **Sécurité** : Hashage bcrypt des mots de passe
- **Profil Utilisateur** : Gestion des informations personnelles

## 🚀 Installation et Démarrage

### Prérequis

- **Flutter** 3.0+
- **Python** 3.8+
- **PostgreSQL** 12+
- **Node.js** 16+ (pour le serveur de développement)

### Installation Rapide

1. **Cloner le projet**
```bash
git clone <repository-url>
cd OMNI.AFRICA.AI
```

2. **Démarrer avec le script automatique**
```bash
# Windows
start_app.ps1

# Linux/Mac
./start_app.sh
```

### Installation Manuelle

#### Frontend Flutter

```bash
cd frontend

# Installer les dépendances
flutter pub get

# Lancer l'application
flutter run -d chrome
```

#### Backend Python

```bash
cd backend

# Créer l'environnement virtuel
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate     # Windows

# Installer les dépendances
pip install -r requirements.txt

# Configurer la base de données
createdb omni_africa_ai

# Démarrer le serveur
python app.py
```

## 📱 Utilisation

### 1. **Accueil et Navigation**
- Écran de démarrage avec logo animé
- Navigation intuitive vers les fonctionnalités
- Accès rapide à l'authentification

### 2. **Authentification**
- Création de compte avec validation
- Connexion sécurisée
- Gestion du profil utilisateur

### 3. **Saisie des Besoins**
- **Formulaire Textuel** : Description détaillée
- **Saisie Vocale** : Reconnaissance multilingue
- **Sélection du Secteur** : Choix parmi 12 secteurs
- **Taille d'Entreprise** : Petite, moyenne, grande

### 4. **Analyse IA**
- Traitement intelligent des besoins
- Génération d'analyses personnalisées
- Recommandations d'outils adaptés

### 5. **Résultats et Recommandations**
- Affichage des résultats avec synthèse vocale
- Liste d'outils recommandés par secteur
- Détails et liens vers les outils
- Possibilité d'arrêter la lecture audio

## 🔧 Configuration

### Variables d'Environnement

#### Frontend (Flutter)
```dart
// lib/core/constants/app_constants.dart
static const String baseUrl = 'https://doudou-app.com';
static const String localUrl = 'http://localhost:8000';
```

#### Backend (Python)
```env
# backend/config.env
FLASK_ENV=development
DATABASE_URL=postgresql://postgres:ouda@localhost:5432/omni_africa_ai
GEMINI_API_KEY=your-gemini-api-key
```

### Base de Données

```sql
-- Créer la base de données
CREATE DATABASE omni_africa_ai;

-- Appliquer les migrations
flask db upgrade
```

## 🧪 Tests

### Frontend
```bash
cd frontend
flutter test
```

### Backend
```bash
cd backend
python -m pytest tests/
```

## 📊 Monitoring et Logs

### Frontend
- Logs de développement dans la console
- Gestion des erreurs réseau
- Analytics intégrés

### Backend
- Logs structurés dans `backend/logs/`
- Monitoring des performances
- Health checks automatiques

## 🔄 Déploiement

### Production

#### Frontend
```bash
cd frontend
flutter build web
# Déployer le dossier build/web/
```

#### Backend
```bash
cd backend
gunicorn -w 4 -b 0.0.0.0:8000 app:app
```

### Docker
```bash
# Build des images
docker build -t omni-africa-ai-frontend ./frontend
docker build -t omni-africa-ai-backend ./backend

# Lancer les conteneurs
docker-compose up -d
```

## 🛠️ Développement

### Structure Modulaire

#### Frontend
- **Core** : Constantes, configuration, routes, utilitaires
- **Screens** : Écrans organisés par fonctionnalité
- **Services** : API et intégrations externes
- **Widgets** : Composants réutilisables
- **Models** : Modèles de données

#### Backend
- **Routes** : Endpoints API organisés
- **Services** : Logique métier
- **Models** : Modèles de base de données
- **Utils** : Utilitaires et helpers
- **Middleware** : Authentification, CORS, rate limiting

### Ajouter une Nouvelle Fonctionnalité

1. **Frontend** : Créer l'écran dans `screens/`
2. **Backend** : Ajouter la route dans `routes/`
3. **Base de données** : Créer le modèle dans `database/models.py`
4. **Tests** : Ajouter les tests correspondants

## 📋 Bonnes Pratiques

### Code
- **Séparation des responsabilités**
- **Code modulaire et réutilisable**
- **Documentation claire**
- **Tests automatisés**
- **Gestion d'erreurs robuste**

### Sécurité
- **Authentification JWT**
- **Hashage des mots de passe**
- **Validation des données**
- **Protection CORS**
- **Rate limiting**

### Performance
- **Optimisation des requêtes**
- **Cache intelligent**
- **Chargement lazy**
- **Compression des assets**

## 🤝 Contribution

### Guidelines
1. Fork le projet
2. Créer une branche feature (`git checkout -b feature/AmazingFeature`)
3. Commit les changements (`git commit -m 'Add AmazingFeature'`)
4. Push vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrir une Pull Request

### Standards de Code
- **Flutter** : Suivre les conventions Dart
- **Python** : PEP 8 pour le style
- **Tests** : Couverture minimale de 80%
- **Documentation** : Docstrings pour toutes les fonctions

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 📞 Support

- **Email** : support@omni-africa-ai.com
- **Documentation** : https://docs.omni-africa-ai.com
- **Issues** : GitHub Issues

## 🙏 Remerciements

- **Google Gemini AI** pour l'intelligence artificielle
- **Flutter Team** pour le framework mobile
- **Flask Community** pour le framework web
- **Tous les contributeurs** qui participent au projet

---

**OMNI.AFRICA.AI** - Transformons ensemble l'avenir numérique de l'Afrique ! 🌍✨ 