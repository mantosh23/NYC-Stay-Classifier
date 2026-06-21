# NYC Stay Classifier

Machine learning classification pipeline and web application that predicts whether an NYC short-term rental listing is an **Entire home/apt**, **Private room**, or **Shared room** based on location, pricing, availability, and review metrics.

## Project Structure

- `nyc_stay_classifier.ipynb` — Exploratory data analysis, preprocessing pipeline, model comparison, hyperparameter tuning, and model serialization
- `Model_Pipeline.pkl` — Serialized scikit-learn preprocessing and classification pipeline
- `main.py` — FastAPI backend exposing health check (`GET /`) and prediction (`POST /predict`) endpoints
- `index.html`, `style.css`, `script.js` — Interactive web interface for testing listing predictions
- `requirements.txt` — Python dependencies
- `runtime.txt` — Python runtime specification (`python-3.12.7`)

## Running Locally

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Start the FastAPI server:
   ```bash
   uvicorn main:app --reload
   ```

3. Serve the frontend (in a separate terminal):
   ```bash
   python3 -m http.server 5500
   ```
   Then open `http://127.0.0.1:5500` in your browser. (`script.js` is configured for `http://127.0.0.1:8000` by default.)
