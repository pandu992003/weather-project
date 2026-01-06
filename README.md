# Weather Agent Microservice Project

This project consists of two main components:
1. **Server (FastAPI + MCP)**: Handles weather API logic.
2. **Client (Streamlit)**: Provides a chat interface for the user.

## 📂 Structure
- `server/`: Backend code.
- `client/`: Frontend code.
- `keys/`: (Optional) Deployment keys.

## 🚀 How to Run (Local - No Docker)

**Prerequisite:** Ensure you are in the root directory `weather_project - Copy (2)`.

### 1️⃣ Start the Server (Terminal 1)
```powershell
pip install -r server/requirements.txt
python server/main.py
```
*(Runs on Port 8001 to avoid conflicts)*

### 2️⃣ Start the Client (Terminal 2)
```powershell
pip install -r client/requirements.txt
# Use 'python -m streamlit' to avoid version conflicts
$env:SERVER_URL="http://localhost:8001/mcp/sse"; python -m streamlit run client/app.py
```

---

## 🐳 How to Run (With Docker)
```bash
docker-compose up --build
```
- The **Client** will be available at: [http://localhost:8501](http://localhost:8501)
- The **Server** will be available at: `http://localhost:8001` (Internal)
