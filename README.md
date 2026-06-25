# 🔗 URL Shortener

A full-stack URL Shortener web application built with **FastAPI**, **React**, and **PostgreSQL** — featuring user authentication, custom short codes, click tracking, and Docker support.

---

## 🚀 Features

- Shorten long URLs into clean, shareable links
- User authentication with JWT
- Custom short code support
- Click analytics tracking
- REST API with FastAPI
- Dockerized setup for easy deployment
- Database migrations with Alembic
- Frontend built with React

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | FastAPI (Python) |
| Frontend | React |
| Database | PostgreSQL |
| ORM / Migrations | SQLAlchemy + Alembic |
| Auth | JWT (JSON Web Tokens) |
| Containerization | Docker + Docker Compose |
| Testing | Pytest |

---

## 📁 Project Structure

URL_Shortener/

├── app/               # FastAPI backend (routes, models, auth, config)

├── frontend/          # React frontend

├── alembic/           # Database migrations

├── tests/             # Pytest test cases

├── .env               # Environment variables (not committed)

├── docker-compose.yml # Docker Compose config

└── alembic.ini        # Alembic configuration

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.10+
- Node.js
- Docker & Docker Compose (optional but recommended)
- PostgreSQL

---

### 1. Clone the Repository

```bash
git clone https://github.com/Asthag0yal/url-shortner.git
cd url-shortner
```

---

### 2. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/urlshortener
SECRET_KEY=your_secret_key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

---

### 3. Run with Docker (Recommended)

```bash
docker-compose up --build
```

App will be available at `http://localhost:8000`

---

### 4. Run Locally (Without Docker)

**Backend:**

```bash
# Create virtual environment
python -m venv .venv
.venv\Scripts\activate        # Windows
source .venv/bin/activate     # Mac/Linux

# Install dependencies
pip install -r requirements.txt

# Run migrations
alembic upgrade head

# Start FastAPI server
uvicorn app.main:app --reload
```

**Frontend:**

```bash
cd frontend
npm install
npm start
```

---

## 📬 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/auth/register` | Register a new user |
| POST | `/auth/login` | Login and get JWT token |
| POST | `/urls/shorten` | Create a short URL |
| GET | `/{short_code}` | Redirect to original URL |
| GET | `/urls/my-urls` | Get all URLs for logged-in user |
| DELETE | `/urls/{id}` | Delete a URL |

---

## 🧪 Running Tests

```bash
pytest tests/
```

---

## 👩‍💻 Author

**Astha Goyal**
B.Tech Computer Science & AI — JECRC, Jaipur
[GitHub](https://github.com/Asthag0yal) • [LinkedIn](https://linkedin.com/in/astha-goyal)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
