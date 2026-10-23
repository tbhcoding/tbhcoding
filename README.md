<h1 align="center">Blessie Faith S. Bongalos</h1>

<p align="center">
  <strong>Software Developer &middot; Machine Learning, IoT &amp; Full-Stack Systems</strong><br>
  BS Computer Science, Camarines Sur Polytechnic Colleges &middot; Philippines
</p>

<!-- Contact row: fill in both links, then delete these two comment lines.
<p align="center">
  <a href="https://www.linkedin.com/in/your-handle/"><img src="https://skillicons.dev/icons?i=linkedin" height="36" alt="LinkedIn"></a>&nbsp;
  <a href="mailto:you@example.com"><img src="https://skillicons.dev/icons?i=gmail" height="36" alt="Email"></a>
</p>
-->

I build systems that turn sensor and image data into decisions: a deep-learning pipeline that maps pH across multispectral images of meat, a cloud backend that keeps hydroponic reservoirs in range on its own, and a real-time scheduling platform for my campus. My work spans models and data, APIs and databases, and the interfaces people actually use. I care about evidence: seeded, reproducible experiments, honest baselines, and secure-by-default backends.

## Tech Stack

| Area | Tools |
|:--|:--|
| **Languages** | <img src="https://skillicons.dev/icons?i=python,js,ts" height="40" alt="Python, JavaScript, TypeScript"><br><sub>SQL</sub> |
| **Machine Learning & Data** | <img src="https://skillicons.dev/icons?i=pytorch,tensorflow,sklearn,opencv" height="40" alt="PyTorch, TensorFlow, scikit-learn, OpenCV"><br><sub>NumPy · pandas · SciPy · XGBoost · imbalanced-learn · Jupyter</sub> |
| **Backend & Databases** | <img src="https://skillicons.dev/icons?i=fastapi,flask,mysql,postgres,supabase" height="40" alt="FastAPI, Flask, MySQL, PostgreSQL, Supabase"><br><sub>REST APIs · WebSockets · Streamlit</sub> |
| **Frontend & UI** | <img src="https://skillicons.dev/icons?i=angular,html,css" height="40" alt="Angular, HTML, CSS"><br><sub>Flet · Gradio · Plotly</sub> |
| **DevOps & Tools** | <img src="https://skillicons.dev/icons?i=git,github,githubactions,docker,azure" height="40" alt="Git, GitHub, GitHub Actions, Docker, Azure"><br><sub>Railway · pytest · SonarQube</sub> |

## Projects

### Machine Learning & Computer Vision

#### [XpHectra (LIGTAS-pH) — Multispectral pH Mapping](https://github.com/tbhcoding/XPHECTRA)

`PyTorch` `NumPy` `SciPy` `scikit-learn` `OpenCV` `Gradio`

Estimates pH at every pixel of a pork sample from a six-band multispectral image (481–970 nm). A physics-based simulator with literature-constrained optical parameters generates labeled data, and a U-Net-style convolutional regression network reconstructs the full pH map from only four probe readings per sample. On a 500-sample held-out synthetic benchmark across five training seeds it reaches **MAE 0.094 pH** and **R² 0.85 ± 0.04**, and it outperforms linear and PLS regression at every setting of the parameter-sensitivity sweep.

<sub>Thesis project, research team &middot; My role: forward model and synthetic-data generator, literature sourcing of its parameters, reproducibility and metric audits.</sub>

#### [Intelligent Energy Forecasting](https://github.com/tbhcoding/Intelligent-Energy-Forecasting)

`TensorFlow` `pandas` `scikit-learn` `SciPy`

Compares stacked RNN and LSTM networks (64-32-16 units) for next-day household electricity forecasting on the UCI Household Power Consumption dataset, with IQR outlier handling, minute-to-daily resampling, and cyclical time encoding. The LSTM cut MSE by 12.7%, a gap that was not statistically significant; both models are evaluated on MSE, RMSE, MAE, MAPE, R², and MASE.

#### [Sleep Disorder Prediction](https://github.com/tbhcoding/SleepPrediction-ML)

`scikit-learn` `XGBoost` `imbalanced-learn` `pandas` `Plotly`

Multiclass prediction of insomnia, sleep apnea, or no disorder from health and lifestyle data, comparing XGBoost, Gradient Boosting, KNN, and Logistic Regression with SMOTE class balancing and cross-validation. The ensembles and KNN reached roughly 90–92% accuracy, and an interactive ipywidgets tool serves predictions from any of the trained models.

### IoT, Backend & DevOps

#### [HydroFi — Hydroponic Monitoring & Auto-Dosing](https://github.com/tbhcoding/hydrofi)

`FastAPI` `Supabase` `PostgreSQL` `JavaScript` `ESP32` `Railway`

Closed-loop control for hydroponic reservoirs. An ESP32 posts pH, TDS, and water-temperature readings to a FastAPI service backed by Supabase Postgres with row-level security; out-of-range readings queue pump corrections for the device, and a web dashboard shows live and historical data with AUTO/MANUAL control and on-demand dosing. The backend runs on Railway.

<sub>Startup team &middot; My role: database schema, device API contract, and backend (device auth, ingestion, read APIs, command queue, auto-dosing); first dashboard integration; Railway deployment.</sub>

#### [Flask CI/CD Pipeline](https://github.com/tbhcoding/flask-cicd-demo)

`GitHub Actions` `Docker` `Azure` `Flask` `Gunicorn` `pytest`

A GitHub Actions pipeline that runs the pytest suite, builds a Docker image, and on every push to `main` deploys over SSH to an Azure VM, where the container is rebuilt and served by Gunicorn.

### Full-Stack & Web Applications

#### [EduROOM — Classroom Reservation System](https://github.com/tbhcoding/EduROOM)

`Python` `Flet` `MySQL` `WebSockets` `Plotly` `Docker`

Cross-platform scheduling system for CSPC's Academic Building IV: conflict-checked bookings, an approval workflow, and an admin analytics dashboard, with role-based access for students, faculty, and administrators. Security is built in (bcrypt hashing, login lockout, session timeouts, per-session action tokens, parameterized SQL, audit logging), and a WebSocket server pushes updates to every client in real time.

<sub>Team of four &middot; My role: product lead; lead full-stack and backend developer.</sub>

#### [TraceSure — Lost & Found System](https://github.com/tbhcoding/TraceSure-LostAndFound-System)

`Python` `Streamlit` `MySQL` `pandas`

Lost-and-found management on a normalized MySQL schema (items, finders, categories, locations) with item intake, claim-status tracking, search, CSV export, and orphan-record cleanup, documented with an ERD and relational model. [Demo video](https://youtu.be/ItKQRZXjIkM)

#### [Melting Sanctuaries](https://github.com/tbhcoding/MeltingSanctuaries)

`HTML` `CSS` `JavaScript` `particles.js`

Climate-awareness microsite on endangered Arctic and glacial species, with parallax glacier scenes, scroll-triggered transitions, and particle snowfall. [Live site](https://tbhcoding.github.io/MeltingSanctuaries/)

<sub>Team project.</sub>

## Experience & Leadership

- **Founder, HydroFi Agritech Solutions** — affordable, AI-powered hydroponics automation for Filipino farmers: a sensor network, automated nutrient dosing, and farm analytics.
- **Chief Partnership Officer, Startup Founders Association – CSPC Chapter** — sources corporate sponsors and partners for student startup programs such as StartUp Voyage, an ideathon and startup-awareness campaign.
- **Hackathons** — 1st Mayoral Naga City Hackathon (iFLOOD, a BLE-mesh flood-rescue module) · Unleash Hacks 2025 (automated power-outage reporting) · Meralco IDOL Hackathon 2026 (typhoon brownout and restoration forecasting).
