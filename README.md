# Planner

Django REST API (`backend/`) + React/Vite/TypeScript app (`frontend/`).

## First-time setup

```powershell
cd backend
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
python manage.py migrate

cd ..\frontend
npm install
```

## Running locally

Run each in its own terminal:

```powershell
# Terminal 1 - API on http://127.0.0.1:8000
cd backend
.\venv\Scripts\Activate.ps1
python manage.py runserver
```

```powershell
# Terminal 2 - app on http://localhost:5173
cd frontend
npm run dev
```

The Vite dev server proxies `/api/*` to Django, so frontend code can call `fetch('/api/...')` directly.
