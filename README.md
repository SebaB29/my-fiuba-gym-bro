# 🏋️‍♂️ MyFiubaGymBro

**MyFiubaGymBro** is a web platform developed as a project for FIUBA. It is designed to help students stay in shape and keep a healthy track of their habits. The system features a **FastAPI** backend, a **React + TypeScript** frontend, and a **PostgreSQL** database, all orchestrated with Docker and ready for development using DevContainers.

# 📍 Table of Contents
- [📝 Description](#-description)
  - [📦 Core Technologies](#-core-technologies)
  - [🧱 Project Structure](#-project-structure)
- [🚀 Getting Started](#-getting-started)
  - [📋 Prerequisites](#-prerequisites)
  - [⚙️ Installation](#️-installation)
- [💡 Usage](#-usage)
  - [🧪 Local Development (DevContainer)](#-local-development-devcontainer)
  - [🛠️ Manual Backend Setup](#️-manual-backend-setup)
  - [💻 Manual Frontend Setup](#-manual-frontend-setup)
  - [🐳 Docker Compose](#-docker-compose)
- [🤝 Contributing](#-contributing)
- [👥 Team](#-team)
- [📄 License](#-license)

# 📝 Description
A detailed platform for student wellness. It uses a layered architecture (routers, dtos, services, repositories) to ensure scalability and maintainability.

## 📦 Core Technologies
* 🐍 **Python** + **FastAPI** + **SQLAlchemy**
* 🐘 **PostgreSQL** + **Alembic** (Migrations)
* ⚛️ **React** + **TypeScript** + **Vite**
* 🐳 **Docker** + **Docker Compose**
* 🛠️ **DevContainer** for consistent development environments.

## 🧱 Project Structure
```text
.
├── .devcontainer/  # DevContainer configuration
├── backend/        # FastAPI source code
├── frontend/       # React + Vite source code
├── local-running/  # Docker Compose orchestration scripts
├── setup.sh        # Initial setup script
└── README.md
```

# 🚀 Getting Started
## 📋 Prerequisites
* Docker & Docker Compose.
* Visual Studio Code + Dev Containers extension (highly recommended).

## ⚙️ Installation
1. Clone the repository:
   ```bash
   git clone git@github.com:SebaB29/my-fiuba-gym-bro.git
   cd myFiubaGymBro
   ```
2. Environment Variables:\
   Create a `.env` file in the `backend/` folder:
   
   ```env
   DATABASE_URL=postgresql://postgres:secret@db:5432/myfiubagymbro
   ```

# 💡 Usage
## 🧪 Local Development (DevContainer)
1. Open the project folder in VS Code.
2. Click **"Reopen in Container"** when prompted (or use `Ctrl+Shift+P` → `Dev Containers: Reopen in Container`).
3. Services will be available at:
   * Backend: `http://localhost:8000`
   * Frontend: `http://localhost:8080`

## 🛠️ Manual Backend Setup
```bash
cd backend
pip install -r requirements.txt
alembic upgrade head
fastapi run src/main.py --port 8000
```
* API Docs: http://localhost:8000/docs
* Tests: Run `pytest` inside the backend folder.

## 💻 Manual Frontend Setup
```bash
cd frontend
npm install
npm run dev
```
* Access at: http://localhost:8080

## 🐳 Docker Compose
To run everything without DevContainers:
```bash
./start.sh   # Starts all services
./stop.sh    # Stops all services
```

# 🤝 Contributing
1. Fork the project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

# 👥 Team

| Nombre                | Usuario de GitHub                                       |
|-----------------------|---------------------------------------------------------|
| Sebastián Brizuela    | [@SebaB29](https://github.com/SebaB29)                  |
| Federico Solari       | [@FedericoSolari](https://github.com/FedericoSolari)    |
| Luciano Gamberale     | [@lucianogamberale](https://github.com/lucianogamberale)|
| Joaquín Velurtas      | [@joaquinvelurtas](https://github.com/joaquinvelurtas)  |
| Santiago Rocco        | [@SantiagoRocco](https://github.com/SantiagoRocco)      |

# 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
