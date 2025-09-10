# Hybrid RAG-NLP-LLM Tool for Predictive Automotive Maintenance

## Overview

In the fast-paced automotive industry, minimizing vehicle downtime and optimizing maintenance schedules are critical to ensuring operational efficiency, safety, and cost savings. This project introduces a cutting-edge **Hybrid Retrieval-Augmented Generation (RAG) system integrated with Natural Language Processing (NLP) and Large Language Models (LLM)** designed specifically for predictive maintenance in combustion engine vehicles. By leveraging AI-driven insights, the tool analyzes sensor data, logs, and symptoms to predict potential failures, recommend targeted actions, and estimate costs—empowering automotive engineers and fleet managers to shift from reactive to proactive maintenance strategies.

Specialized for internal combustion engines (ICE), this tool ignores electric vehicles (EVs) to focus on high-impact areas like coolant systems, lubrication, and overheating issues. Built with scalability in mind, it demonstrates how AI can reduce unplanned breakdowns by up to 30-50% (based on industry benchmarks), extend engine lifespan, and deliver significant ROI for automotive manufacturers, service centers, and logistics companies.

This repository contains a Jupyter Notebook implementation, ready for deployment on platforms like Google Colab with GPU acceleration for real-time predictions.

## Features

- **Intelligent Input Processing with NLP**: Extracts key entities (e.g., symptoms like "high coolant temp" or components like "radiator") using spaCy to refine queries and improve retrieval accuracy.
- **Retrieval-Augmented Generation (RAG)**: Combines vector search with FAISS and Hugging Face embeddings to pull relevant maintenance knowledge from a domain-specific database, ensuring contextually accurate predictions.
- **Advanced LLM Predictions**: Utilizes the Mistral-7B-Instruct model (fine-tuned for precision) to generate structured outputs, including failure predictions, step-by-step actions, cost estimates in USD, and urgency levels (e.g., immediate or within 1 week).
- **Interactive User Interface**: A sleek, user-friendly UI built with ipywidgets for seamless input and output, simulating a real-world diagnostic tool—ideal for mechanics or engineers on the shop floor.
- **Combustion Engine Focus**: Tailored constraints ensure recommendations are ICE-specific, addressing common issues like overheating, leaks, and lubrication failures while providing actionable, cost-effective insights.
- **Scalable and Extensible**: Easily integrable with IoT sensor feeds or telematics systems for live data analysis, with potential for cloud deployment (e.g., AWS or Azure) in production environments.

This tool not only predicts failures but also quantifies benefits, making it a valuable asset for automotive OEMs aiming to enhance reliability and comply with stringent safety standards.

## Data Source

- **Kaggle Dataset**: Draws from the comprehensive "Automotive Vehicles Engine Health Dataset" on Kaggle (https://www.kaggle.com/datasets/parvmodi/automotive-vehicles-engine-health-dataset), featuring ~19,500 entries of authentic automotive sensor logs.
- **Usage in Project**: Efficiently processes the dataset, converted from CSV to JSON for optimal vectorization and retrieval in the notebook. Key parameters include Engine RPM (905.0-1358.9), Lubricant Oil Pressure (2.9-3.8 bar), Coolant Pressure (1.7-2.9 bar), Coolant Temperature (75-85°C), and Engine Condition (0.5-1.0 scale).
- **Focus**: Targets critical failure indicators such as elevated temperatures at idle or RPM fluctuations, all anonymized to maintain privacy.

## Technology Stack

- **NLP**: spaCy for entity recognition and query refinement.
- **Embeddings & Vector Store**: Hugging Face Transformers (`sentence-transformers/all-MiniLM-L6-v2`) and FAISS for high-speed similarity search.
- **LLM**: Mistral-7B-Instruct-v0.3 via Hugging Face Pipeline, optimized for GPU acceleration (e.g., NVIDIA L4 on Colab).
- **RAG Framework**: LangChain for chaining retrieval and generation components.
- **UI & Visualization**: ipywidgets and IPython for interactive dashboards; Markdown for structured outputs.
- **Environment**: Python 3.12 with dependencies like torch, transformers, and langchain—managed via pip or Colab.

This stack ensures low-latency inference (under 5 seconds per query on GPU) and is optimized for automotive edge computing scenarios.

## Workflow

1. **Input Submission**: User enters vehicle symptoms or logs (e.g., "High engine temperature when speed is above 100 KM/H and AC stopped working").
2. **NLP Processing**: spaCy analyzes the input to extract entities and refine the query for better context.
3. **Knowledge Retrieval**: RAG queries the vector store to fetch top-relevant documents from the maintenance corpus.
4. **LLM Generation**: Mistral-7B processes the augmented prompt (with retrieved context and ICE-specific constraints) to predict failures, suggest actions, estimate costs, and assess urgency.
5. **Output Display**: Structured recommendations are rendered in the UI, focusing on practical, cost-effective steps to prevent downtime.
6. **Iteration & Feedback**: Users can refine inputs for iterative diagnostics, simulating a collaborative tool for automotive teams.

This streamlined workflow integrates AI seamlessly into automotive maintenance pipelines, from diagnostics to repair planning.

## Demo

![Demo Screenshot](https://github.com/AashishSaini16/Hybrid_RAG_NLP_LLM_Tool_for_Predictive_Automotive_Maintenance/blob/main/demo.PNG)
