<div align="center">

# Bonjour, je suis Louis Gaillard 👋

**Développeur IA en alternance chez [Hello Mira](https://www.hello-mira.com)**<br>
RAG et agents LLM · Machine learning en production · Data engineering

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge)](https://www.linkedin.com/in/louis-gaillard-6b575a12b)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:louis.gaillard94@gmail.com)

</div>

---

## 🙋 À propos

Je construis des applications d'IA pensées pour la production : assistants conversationnels (RAG, agents LLM), modèles de machine learning servis par API, pipelines de données. Ce qui me plaît, c'est d'emmener un modèle du notebook jusqu'à un service qui tourne, avec les tests, la CI/CD et le monitoring qui vont avec.

- 💼 **Aujourd'hui** : développeur IA en alternance chez Hello Mira, startup lilloise qui construit une plateforme pour les voyageurs et les nomades digitaux. J'y développe des fonctionnalités d'IA utilisées en production.
- 🎓 **Formation** : Développeur en intelligence artificielle chez Simplon Hauts-de-France, à Lille. Je passe le titre RNCP37827 en janvier 2027.
- 📫 **Me joindre** : [LinkedIn](https://www.linkedin.com/in/louis-gaillard-6b575a12b) ou [louis.gaillard94@gmail.com](mailto:louis.gaillard94@gmail.com)

## 🔭 En ce moment

- 🏛️ **ParlIA Mini**, mon projet de certification : à partir du titre et du texte d'une question écrite, il propose au collaborateur d'un sénateur les trois ministères les plus probables pour y répondre. Je le construis de bout en bout sur les données publiques du Sénat : collecte, base SQL, API de données, modèle, API du modèle, application web et tests. Le dépôt sera public avant la remise.
- 📡 **Ma veille tourne toute seule** : mon [bot n8n](https://github.com/lougail/veille-tech-n8n) lit 61 sources deux fois par jour et publie les meilleurs articles sur Discord.
- 🛠️ **Je code avec des agents** (Claude Code) et je construis mes propres outils autour, comme ce [tableau de bord de suivi de projets](https://github.com/lougail/claude-toolkit-dashboard).

## 🧭 Ce que je sais faire

| Compétence | Où le voir |
|---|---|
| Construire un assistant LLM : RAG, agent avec outils, vision | [Chatbot RNCP](https://github.com/lougail/chatbot-rncp-dev-ia) · [Flight Platform](https://github.com/lougail/hello-mira-flight-platform) · [Gaming Advisor](https://github.com/lougail/Gaming-advisor) · [Agent IA citoyen](https://github.com/lougail/ai-agent-with-langchain) |
| Entraîner, évaluer et comparer des modèles | [Priorisation des secours](https://github.com/lougail/accidents_routiers) · [Pneumonie sur radiographies](https://github.com/lougail/TL_classification_images_medicales_v2) · [Prix immobilier](https://github.com/lougail/predicteur_prix_immobilier) |
| Servir un modèle par API et le livrer | [Prix immobilier](https://github.com/lougail/predicteur_prix_immobilier) (API FastAPI) · [Priorisation des secours](https://github.com/lougail/accidents_routiers) (API, CI/CD, images Docker publiées sur GHCR) |
| Superviser une application | [Priorisation des secours](https://github.com/lougail/accidents_routiers) (Prometheus, Grafana, alertes, tests de charge) · [Flight Platform](https://github.com/lougail/hello-mira-flight-platform) (Prometheus, Grafana) |
| Modéliser et transformer des données | [Churn Olist](https://github.com/lougail/brief-olist-churn) (PostgreSQL) · [NYC Taxi](https://github.com/lougail/brief-snowflake-dbt-nyc-taxi) (Snowflake, dbt) · [PySpark](https://github.com/lougail/pyspark-data-processing-tutorial) · [Hadoop](https://github.com/lougail/hadoop-mapreduce-exercises) |
| Collecter des données | Scraping : [veille concurrentielle](https://github.com/lougail/Web_scraping_project) · API publiques : [Flight Platform](https://github.com/lougail/hello-mira-flight-platform) · flux RSS : [veille tech](https://github.com/lougail/veille-tech-n8n) |
| Automatiser | Workflows [n8n](https://github.com/lougail/veille-tech-n8n) · GitHub Actions · Docker Compose |

## 🚀 Projets phares

### 🎓 [Chatbot RNCP Dev IA](https://github.com/lougail/chatbot-rncp-dev-ia)
*« Mon projet couvre-t-il le référentiel ? » Le chatbot répond, citations à l'appui.*

- RAG de bout en bout : le référentiel PDF de 62 pages est découpé en morceaux de 512 caractères, vectorisé avec `mistral-embed` et stocké dans Qdrant ; Mistral Small génère la réponse
- Classe chaque compétence en couverte, à approfondir ou manquante, et affiche ses sources
- Seuil de similarité : une question hors sujet reçoit une réponse vide plutôt qu'une invention
- Interface Chainlit en streaming, tests pytest, lint Ruff, CI GitHub Actions, image Docker multistage d'environ 150 Mo

`Python 3.13` `LangChain` `Mistral` `Qdrant` `Chainlit` `Docker` `uv`

### 🚑 [Priorisation des secours](https://github.com/lougail/accidents_routiers)
*Estimer la gravité d'un accident dès l'appel d'urgence, pour envoyer les bons moyens.*

- Données BAAC 2021-2024 et quatre modèles CatBoost, un par niveau d'information disponible pendant l'appel : le ROC-AUC monte de 0,74 à 0,82, avec un rappel autour de 0,8
- API FastAPI qui choisit le modèle selon les champs reçus, interface Streamlit, base PostgreSQL
- CI/CD GitHub Actions (tests, build, release) et images Docker publiées sur GHCR
- Monitoring Prometheus et Grafana (4 tableaux de bord, 5 règles d'alerte), tests de charge Locust jusqu'à 200 utilisateurs simultanés

`CatBoost` `FastAPI` `Streamlit` `PostgreSQL` `Docker` `Prometheus` `Grafana` `Locust`

### ✈️ [Flight Platform](https://github.com/lougail/hello-mira-flight-platform)
*Des informations de vols en temps réel, et un assistant qui répond en langage naturel.*

- Quatre microservices FastAPI : gateway, aéroports, vols et assistant
- La gateway protège l'API Aviationstack : cache MongoDB de 5 minutes, quota de 10 000 appels par mois, circuit breaker et fusion des requêtes identiques, soit environ 70 % d'appels en moins
- Assistant LangGraph et Mistral avec 7 outils, qui répond dans la langue de la question
- Monitoring Prometheus et Grafana, interface Streamlit avec authentification Supabase, le tout sous Docker Compose

`FastAPI` `MongoDB` `LangGraph` `Mistral` `Supabase` `Prometheus` `Docker`

### 📡 [Veille tech automatisée](https://github.com/lougail/veille-tech-n8n)
*61 sources lues pour moi, deux fois par jour.*

- Workflow n8n de 34 nœuds, auto-hébergé sous Docker
- Dédoublonnage, pré-filtre par mots-clés et texte complet récupéré avec Jina Reader
- Mistral Small classe chaque article et lui donne une note de 1 à 10
- Publication sur 6 canaux Discord thématiques, digest quotidien et hebdomadaire, alerte en cas de panne

`n8n` `Mistral Small` `OpenRouter` `Jina Reader` `Discord` `Docker`

### ❄️ [Pipeline NYC Taxi](https://github.com/lougail/brief-snowflake-dbt-nyc-taxi)
*Un entrepôt de données propre et testé sur les courses des taxis new-yorkais.*

- Snowflake en trois couches : RAW (brut), STAGING (nettoyé), FINAL (indicateurs)
- Modèles dbt staging, intermediate et marts : résumé quotidien, analyse par zone, tendances horaires
- Tests de schéma et 5 tests métier : pas de tarif négatif, départ avant arrivée, vitesse plausible…

`Snowflake` `dbt` `SQL`

### 🛒 [Churn Olist](https://github.com/lougail/brief-olist-churn)
*Préparer les données qui permettront de repérer les clients sur le départ.*

- Environ 100 000 commandes e-commerce normalisées en 8 tables PostgreSQL 16, avec clés et contraintes
- 5 anomalies de qualité corrigées, 9 indicateurs par client calculés avec 7 CTE et des window functions
- Vue `v_customer_features`, index et vue matérialisée, tableau de bord Streamlit

`PostgreSQL 16` `SQL avancé` `Docker` `Streamlit`

## 🤝 Projets d'équipe

### 🎲 [Gaming Advisor](https://github.com/lougail/Gaming-advisor)
*Un assistant IA pour les jeux de société : une photo de la boîte, et il guide la mise en place et répond sur les règles.*

- Analyse des photos avec GPT-4 Vision (Azure OpenAI) et OCR des règles, recherche dans les règles par RAG (pgvector)
- API FastAPI en Clean Architecture (DDD), SQLAlchemy asynchrone, Alembic, JWT, traitements en arrière-plan avec Redis, stockage Azure Blob
- Front Next.js 15, React 19, TypeScript et Tailwind CSS

`GPT-4 Vision` `pgvector` `FastAPI` `Redis` `Azure` `Next.js`

### ⚖️ [Agent IA citoyen](https://github.com/lougail/ai-agent-with-langchain)
*Un assistant qui répond aux questions sur les droits sociaux et administratifs, à partir de documents officiels. Réalisé à trois pendant la formation Simplon.*

- Agent LangChain avec des outils sur mesure : vérifier une éligibilité, résumer, simplifier
- RAG sur des documents institutionnels (ChromaDB), mémoire de conversation, interface Streamlit
- Fonctionne avec OpenAI, DeepSeek ou un modèle local via Ollama

`LangChain` `ChromaDB` `OpenAI` `Ollama` `Streamlit`

## 📚 Autres projets

| Projet | Ce qu'il fait | Stack |
|---|---|---|
| [Prix immobilier](https://github.com/lougail/predicteur_prix_immobilier) | API qui estime le prix au m² à Lille et Bordeaux, à partir des ventes DVF 2022 | scikit-learn, XGBoost, FastAPI |
| [Pneumonie sur radiographies](https://github.com/lougail/TL_classification_images_medicales_v2) | Compare MobileNetV2 et ResNet50 en transfer learning, expériences suivies dans MLflow | TensorFlow, Keras, MLflow |
| [Cancer du sein](https://github.com/lougail/LouisG_ML_challenge_logistic_regression_breast_cancer_wisconsin) | Classe les tumeurs en bénignes ou malignes par régression logistique | scikit-learn |
| [Veille concurrentielle](https://github.com/lougail/Web_scraping_project) | Collecte plus de 1 000 livres, garde l'historique des prix et du stock, les expose par API | Scrapy, FastAPI, SQLAlchemy |
| [Tutoriel PySpark](https://github.com/lougail/pyspark-data-processing-tutorial) | Tutoriel interactif : DataFrames, Spark SQL, RDD, export Parquet | PySpark, Jupyter |
| [Hadoop MapReduce](https://github.com/lougail/hadoop-mapreduce-exercises) | Calculs distribués en Python sur Azure HDInsight | Hadoop Streaming, Azure |
| [Tableau de bord Claude Code](https://github.com/lougail/claude-toolkit-dashboard) | Suit mes projets menés avec Claude Code : état Git et CI, avancement des fonctionnalités, consommation de tokens | Next.js, TypeScript |
| [GitHub Users API](https://github.com/lougail/github-users-api) | API REST sur des profils GitHub filtrés | FastAPI |
| [Réservation de séances](https://github.com/lougail/django-coach-rdv) | Prise de rendez-vous en ligne entre un coach et ses clients, avec calendrier interactif | Django, FullCalendar, Tailwind CSS |
| [Site de restaurant](https://github.com/lougail/restaurant) | Site web d'un restaurant | Laravel 9, PHP |

## 🛠️ Stack technique

| Domaine | Outils |
|---|---|
| **IA générative** | ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langgraph&logoColor=white) ![Mistral AI](https://img.shields.io/badge/Mistral%20AI-FA520F?style=flat&logo=mistralai&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat) ![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat&logo=huggingface&logoColor=black) ![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat&logo=qdrant&logoColor=white) ![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=flat) ![pgvector](https://img.shields.io/badge/pgvector-336791?style=flat&logo=postgresql&logoColor=white) ![Chainlit](https://img.shields.io/badge/Chainlit-F80061?style=flat) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white) |
| **Machine learning** | ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white) ![CatBoost](https://img.shields.io/badge/CatBoost-FFCC00?style=flat) ![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=flat) ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white) ![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white) ![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white) |
| **Back-end et API** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white) ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white) ![Scrapy](https://img.shields.io/badge/Scrapy-60A839?style=flat&logo=scrapy&logoColor=white) |
| **Données** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white) ![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white) ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat) ![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apachespark&logoColor=white) ![Hadoop](https://img.shields.io/badge/Hadoop-66CCFF?style=flat&logo=apachehadoop&logoColor=black) ![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white) ![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat&logo=supabase&logoColor=black) |
| **DevOps et qualité** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white) ![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat&logo=ruff&logoColor=black) ![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat&logo=uv&logoColor=white) ![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat) |
| **Front-end** | ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat&logo=tailwindcss&logoColor=white) |

## 📈 Activité GitHub

<p align="center">
  <img src="https://github-stats-extended.vercel.app/api?username=lougail&show_icons=true&theme=tokyonight&hide_rank=true&hide=stars,issues,contribs&show=prs_merged" alt="Statistiques GitHub" height="165">
  <img src="https://github-stats-extended.vercel.app/api/top-langs/?username=lougail&layout=compact&theme=tokyonight&langs_count=6&hide=jupyter%20notebook" alt="Langages les plus utilisés" height="165">
</p>
