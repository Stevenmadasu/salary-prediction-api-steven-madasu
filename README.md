# Salary Prediction API

## BAIS:3300 - Digital Product Development

Flask API that serves a trained Random Forest salary prediction model.

### Live Deployment
🌐 **Azure App Service**: https://salary-predict-bob.azurewebsites.net

### Endpoints

#### `GET /`
Returns a welcome page confirming the API is running.

#### `POST /predict`
Accepts JSON payload and returns predicted salary.

**Request body:**
```json
{
    "age": 7,
    "gender": 0,
    "country": 55,
    "highest_deg": 3,
    "coding_exp": 4,
    "title": 13,
    "company_size": 2
}
```

**Response:**
```json
{
    "predicted_salary": 108383.37084646407
}
```

### Files
- `app.py` - Flask application with `/` and `/predict` routes
- `salary_predict_model.pkl` - Trained Random Forest model
- `requirements.txt` - Python dependencies

### Deployment
Deployed to Azure App Service (Python 3.12, F1 Free tier) with gunicorn.

### Author
Bob
