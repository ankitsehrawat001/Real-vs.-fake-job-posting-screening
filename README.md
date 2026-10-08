# JobShield: Real vs. Fake Job Posting Prediction

JobShield is a Streamlit app that analyzes a job description and predicts whether its text resembles a real or potentially fraudulent posting. It uses the project's trained TF-IDF vectorizer and SVM classification model.

## Features

- Paste a job description into the web form and request a prediction.
- See a clear result with practical reminders for reviewing a job posting.
- Run the included trained model locally.

## Project files

| File | Purpose |
| --- | --- |
| `app.py` | Streamlit interface and prediction logic |
| `fake_job_tfidf.joblib` | Trained text vectorizer |
| `fake_job_svm_model.joblib` | Trained SVM classifier |
| `Real_Fake_Job_Posting_Prediction.ipynb` | Notebook containing the project workflow |
| `requirements.txt` | Python package dependencies |

## Requirements

- Python 3.9 or later
- pip

## Run locally

Open a terminal in the project directory, then create and activate a virtual environment.

### Windows PowerShell

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### macOS or Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the dependencies and start the app:

```bash
pip install -r requirements.txt
streamlit run app.py
```

Streamlit will print a local URL (usually `http://localhost:8501`) to open in your browser.

The model files `fake_job_tfidf.joblib` and `fake_job_svm_model.joblib` must remain in the same directory as `app.py`.

## Use the app

1. Paste the full job description into the text box.
2. Select **Analyze job posting**.
3. Review the model result and verify the employer and role independently.

The classifier uses the job description text. Include relevant details such as responsibilities, requirements, compensation, and application instructions when available.

## Limitations

The result is a model prediction based on text patterns, not a guarantee or a substitute for independent verification. A legitimate posting may be flagged, and a fraudulent posting may not be detected. Do not share sensitive personal information or pay an employer to apply without verifying the request through trusted channels.

## Dependencies

Dependencies are listed in [`requirements.txt`](requirements.txt).
