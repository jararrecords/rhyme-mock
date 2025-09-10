# RhymeSphere Mock Server (Full)

This FastAPI mock server provides a full in-memory backend for RhymeSphere to test User & Admin Android apps.

## Endpoints
Visit `/api/v1/docs` after deploying to see the interactive Swagger UI.

## Deploy to Railway
1. Push this repo to GitHub (create repo `rhyme-mock`).
2. In Railway, choose Deploy -> GitHub Repo and select this repo.
3. Railway will use `requirements.txt` and `Procfile` to run the app.
4. After deploy, update your Android apps `RetrofitClient.kt` base URL to:
   `https://<your-app>.up.railway.app/api/v1/`

## Run locally
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python -m uvicorn mock_server.main:app --reload --port 8000
```
