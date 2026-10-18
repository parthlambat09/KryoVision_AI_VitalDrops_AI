# 🏗️ KryoVision System Architecture

This document outlines the technical architecture, data flow, and AI compliance for the KryoVision Autonomous Cold-Chain Intelligence platform.

## 1. High-Level Architecture
KryoVision operates on a microservices-based architecture bridging edge IoT hardware with cloud-based AI inference.

*   **Edge Layer (IoT):** ESP32 microcontrollers equipped with DHT22 (Dual-zone Temp/Humidity), MQ-3 (VOC/Ethylene), and an optical camera module (Spore-trap).
*   **Data Ingestion:** MQTT protocol streams telemetry to the backend. Offline scenarios are handled via a local PWA cache that syncs upon reconnection.
*   **Backend Engine:** FastAPI (Python) handles high-throughput asynchronous data streams and serves the REST/WebSocket APIs.
*   **Database:** PostgreSQL with TimescaleDB extension for time-series sensor data and Redis for caching alerts.
*   **Frontend:** Next.js (React) for the Mission Control dashboard, utilizing TailwindCSS for styling and Mapbox GL for dynamic route visualization.

## 2. Artificial Intelligence Modules
Our solution integrates three distinct AI paradigms:

1.  **Optical Spore Detection (Edge CNN):** A lightweight Convolutional Neural Network (CNN) analyzes images from the spore-trap chamber to detect *Botrytis* and *Aspergillus* bio-aerosols.
2.  **Dynamic RSL Engine (ML):** A predictive kinetic decay model utilizing Arrhenius equations to compute Remaining Shelf Life based on accumulated thermal abuse.
3.  **GenAI Dispute Arbiter (LLM & XAI):** An LLM agent (via LangChain) that parses IoT telemetry and digital SLAs to output transparent, insurance-ready claim dockets. Designed with Explainable AI (XAI) principles to ensure objective liability apportionment.

## 3. Mandatory AI Disclosure (FTL 5.0 Compliance)
In compliance with the FTL 5.0 Rulebook, we disclose the following regarding AI generation in our codebase:

*   **AI Tools Used:** GitHub Copilot, Gemini 1.5 Pro.
*   **Purpose:** Boilerplate generation, Tailwind CSS scaffolding, and syntax debugging.
*   **Code Contribution:** AI-generated code accounts for **< 15%** of the overall codebase. 
*   **Custom Logic:** Over **85%** of the core logic—including the FastAPI routing, MQTT ingestion, Arrhenius decay algorithms, and XAI dispute arbitration prompts—was custom-written by the team.
