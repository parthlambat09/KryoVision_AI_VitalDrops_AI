# 👥 Team Contributions & Accountability

In compliance with the FTL 5.0 Rulebook, this document logs the roles, responsibilities, and contributions of each team member. 

**Team Name:** [Insert Team Name]
**Track:** [Insert Chosen Track, e.g., Full Stack / ML & Anomaly Detection]

## 👨‍💻 Member Roles & Contributions

### 1. Parth Lambat (Tech Lead / AI Architect)
*   **Responsibilities:** Core AI architecture, CNN optical spore detection model, and GenAI Dispute Arbiter logic.
*   **Key Contributions:** 
    *   Trained and integrated the edge CNN model for *Botrytis* spore detection.
    *   Developed the LangChain pipeline for the Explainable AI (XAI) Dispute Arbiter.
    *   Designed the Arrhenius kinetic decay model for RSL prediction.
*   **Primary Commits:** `ml_models/`, `llm_agent/`, `ARCHITECTURE.md`

### 2. Omkar (Backend Developer / AI Integration)
*   **Responsibilities:** FastAPI backend development, database architecture, and IoT telemetry pipelines.
*   **Key Contributions:** 
    *   Built the MQTT/WebSocket telemetry ingestion and streaming endpoints.
    *   Integrated the RSL ML model and GenAI Arbiter into the FastAPI routes.
    *   Developed the autonomous distress rerouting logic API.
*   **Primary Commits:** `server/api/`, `server/main.py`, `server/models/`

### 3. Aishwarya Joshi (Frontend Developer / UI/UX)
*   **Responsibilities:** UI/UX design, Next.js dashboard development, and data visualization.
*   **Key Contributions:** 
    *   Built the Mission Control dashboard and Smart Booking Wizard.
    *   Integrated Recharts/Chart.js for live telemetry gauges.
    *   Implemented Mapbox GL for live truck routing and dynamic re-routing visuals.
*   **Primary Commits:** `client/components/`, `client/app/`, `tailwind.config.js`

### 4. Akash (Data Engineer / QA)
*   **Responsibilities:** IoT data simulation, dataset preparation, and API testing.
*   **Key Contributions:** 
    *   Developed the Python IoT Telemetry Simulator script to generate realistic sensor data.
    *   Prepared the training datasets for the CNN optical spore detection model.
    *   Conducted API load testing and validated WebSocket connectivity.
*   **Primary Commits:** `simulator/telemetry_sim.py`, `data/`, `tests/api_tests.py`

### 5. Pallavi (Project Manager / QA & Documentation)
*   **Responsibilities:** SLA contract generation, PDF docket formatting, and rulebook compliance.
*   **Key Contributions:** 
    *   Wrote the mock digital Service Level Agreements (SLAs) for the LLM to parse.
    *   Built the Python module that formats the LLM output into an insurance-ready PDF claim docket.
    *   Ensured documentation compliance (`SETUP.md`, open-source attribution).
*   **Primary Commits:** `server/utils/pdf_gen.py`, `docs/`, `mock_slas/`

---
*Note: A complete commit history proving daily, meaningful commits from all members can be verified in the GitHub repository's commit graph.*
