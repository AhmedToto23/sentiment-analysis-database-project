# 🧠 Sentiment Analysis Social Media Platform

A **full-stack social media platform** with integrated **AI-powered sentiment analysis**, real-time interactions, and advanced analytics dashboards.  
This project combines modern web technologies with **NLP and data analytics** to provide insights into user emotions and engagement trends.

---

## 📋 Table of Contents

- [Overview](#-overview)

- [Key Features](#-key-features)

- [Project Architecture](#-project-architecture)

- [Technology Stack](#-technology-stack)

- [Installation](#-installation)

- [Configuration](#-configuration)

- [Running the Application](#-running-the-application)

- [API Documentation](#-api-documentation)

- [Database Schema](#-database-schema)

- [Contributing](#-contributing)

- [License](#-license)

- [Acknowledgments](#-acknowledgments)

---

## 🌟 Overview

This project is a **modern social media application** that extends traditional social networking features with **AI-driven sentiment analysis**.


Users can:
- Create and interact with content
- Receive real-time feedback
- Explore **sentiment trends and emotional analytics**
- Visualize engagement through interactive dashboards

The platform is built using a **FastAPI + React** architecture with **Streamlit-based analytics dashboards**.

---

## ✨ Key Features

### 🔐 Core Social Features

- **Authentication & Authorization**

  - Secure JWT-based authentication

- **Post Management**

  - Create, read, update, and delete posts

  - Media upload support

- **Real-Time Interactions**

  - Likes, comments, bookmarks, follows

- **User Profiles**

  - Custom avatars and bios

- **Notifications System**

  - Real-time interaction updates

- **Stories**

  - Temporary content sharing

- **Feed Algorithm**

  - Personalized content discovery

---

### 🤖 AI-Powered Features

- **Sentiment Analysis**

  - Automatic sentiment detection for posts & comments

- **Real-Time Sentiment Classification**

  - Positive 😊 | Neutral 😐 | Negative 😡

- **NLP Model**

  - `cardiffnlp/twitter-roberta-base-sentiment`

- **Sentiment Analytics Dashboard**

  - Track emotional patterns over time

---

### 📊 Analytics & Reporting

- **User Analytics**

  - Growth, activity, and engagement metrics

- **Post Analytics**

  - Trending, most liked, most commented posts

- **Sentiment Trends**

  - Emotional insights across time periods

- **Engagement Metrics**

  - Interaction-level analytics

- **Custom SQL Dashboard**

  - Advanced analytics using raw SQL queries

---

## 📁 Project Architecture

```text
sentiment-analysis-database-project/

│

├── backend/

│   ├── alembic/

│   ├── app/


│   │   ├── api/

│   │   │   └── v1/

│   │   ├── core/

│   │   ├── crud/

│   │   ├── models/

│   │   ├── schemas/

│   │   ├── services/

│   │   ├── middleware/

│   │   └── utils/

│   ├── tests/

│   ├── uploads/

│   ├── requirements.txt

│   └── run.py

│

├── frontend/

│   ├── components/

│   ├── context/

│   ├── pages/

│   ├── services/

│   └── package.json

│

├── sentiment-model/

│   ├── app.py

│   └── requirements.txt

│

├── run-queries/

│   ├── queries/

│   ├── app.py

│   ├── database.py

│   └── requirements.txt

│

├── ERD.png

├── Mapping.png

├── Tables.sql

├── Creating Queries.sql

└── Documentation.pdf


## 🛠 Technology Stack

### Backend
- **FastAPI** 0.109.0  
- **SQL Server**  
- **SQLAlchemy** 2.0  
- **Alembic**  
- **JWT Authentication**  
- **Uvicorn**

### Frontend
- **React.js**  
- **Tailwind CSS**  
- **Axios**  
- **React Context API**

### AI / Machine Learning
- **Transformers (Hugging Face)**  
- **PyTorch**  
- **Model:** `cardiffnlp/twitter-roberta-base-sentiment`

### Analytics
- **Streamlit**  
- **Built-in Visualizations**

---

## 🚀 Installation

### Prerequisites
- Python **3.12+**
- Node.js **16+**
- SQL Server
- Git

---

### Backend Setup

```bash
git clone <repository-url>
cd sentiment-analysis-database-project/backend

```bash
python -m venv env

```bash
# Windows
env\Scripts\activate
# Linux / macOS
source env/bin/activate

```bash
pip install -r requirements.txt


## Create a .env file:
```bash
DATABASE_URL=mssql+pyodbc://username:password@server/database?driver=ODBC+Driver+17+for+SQL+Server
SECRET_KEY=your-secret-key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

```bash
alembic upgrade head


## Frontend Setup

```bash
cd ../frontend
npm install
npm start


## Sentiment Model

```bash
cd ../sentiment-model
pip install -r requirements.txt
streamlit run app.py


## Analytics Dashboard

```bash
cd ../run-queries
pip install -r requirements.txt
streamlit run app.py


## 🏃 Running the Application

Backend

```bash
uvicorn app.main:app --reload

- API: http://localhost:8000

- Docs: http://localhost:8000/docs

Frontend

```bash
npm start


- App: http://localhost:3000


## 📚 API Documentation


### Authentication

- `POST /api/v1/auth/register`

- `POST /api/v1/auth/login`

- `POST /api/v1/auth/refresh`


### Posts

- `GET /api/v1/posts`

- `POST /api/v1/posts`

- `PUT /api/v1/posts/{id}`

- `DELETE /api/v1/posts/{id}`


### Analytics

- `GET /api/v1/analytics/sentiment-trends`

- `GET /api/v1/analytics/engagement`

---

## 🗄️ Database Schema


Main tables:

- **Users**

- **Posts**

- **Comments**

- **Reactions**

- **Sentiments**

- **Follows**

- **Bookmarks**

- **Notifications**

- **Stories**

---

## 📝 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgments
- CardiffNLP  
- FastAPI Community  
- React Ecosystem  
- Streamlit Team  

---
