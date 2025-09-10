# Hybrid RAG-NLP-LLM Tool for Predictive Automotive Maintenance

## Overview

This cutting-edge AI tool harnesses **Hybrid Retrieval-Augmented Generation (RAG)** integrated with **Natural Language Processing (NLP)** and **Large Language Models (LLM)** to deliver advanced predictive maintenance for combustion engine vehicles. By analyzing real-time sensor logs, it accurately forecasts potential failures, provides actionable recommendations, estimates costs in USD, and evaluates urgency levels—empowering automotive fleets to minimize downtime, boost operational efficiency, enhance vehicle safety, and achieve substantial cost savings. Built on authentic datasets and aligned with Industry 4.0 standards, this solution excels in proactive diagnostics for trucks, heavy machinery, and beyond, making it an indispensable asset for modern automotive engineering.

## Features

- **NLP Query Refinement**: Leverages spaCy for precise entity extraction (e.g., identifying "coolant temp" or "truck XYZ") to optimize input and retrieval accuracy.
- **RAG-Based Retrieval**: Employs advanced embeddings and FAISS for seamless, context-rich searches across vast sensor data.
- **LLM-Driven Predictions**: Utilizes Mistral-7B to generate insightful, structured outputs including failure predictions, targeted actions, cost estimates, and urgency assessments (e.g., "immediate" for critical overheating scenarios).
- **Multi-Constraint Recommendations**: Delivers practical USD-based cost breakdowns (e.g., $100-300 for cooling system repairs) alongside time-sensitive urgency ratings.
- **Interactive UI**: Features an intuitive ipywidgets interface for effortless log input and instant, real-time results.
- **Dataset Grounding**: Guarantees reliable, fact-based responses deeply rooted in sensor data, eliminating guesswork and ensuring high-fidelity insights.

## Data Source

- **Kaggle Dataset**: Draws from the comprehensive "Automotive Vehicles Engine Health Dataset" on Kaggle (https://www.kaggle.com/datasets/parvmodi/automotive-vehicles-engine-health-dataset), featuring ~19,500 entries of authentic automotive sensor logs.
- **Usage in Project**: Efficiently processes the dataset, converted from CSV to JSON for optimal vectorization and retrieval in the notebook. Key parameters include Engine RPM (905.0-1358.9), Lubricant Oil Pressure (2.9-3.8 bar), Coolant Pressure (1.7-2.9 bar), Coolant Temperature (75-85°C), and Engine Condition (0.5-1.0 scale).
- **Focus**: Targets critical failure indicators such as elevated temperatures at idle or RPM fluctuations, all anonymized to maintain privacy.

## Technology

- **Core**: Python 3.10+, NumPy, Pandas for robust data handling.
- **NLP**: spaCy with the en_core_web_sm model for sophisticated language understanding.
- **RAG**: LangChain for seamless document loading, splitting, and retrieval; HuggingFace Embeddings (all-MiniLM-L6-v2) for high-performance vectorization; FAISS as the vector store for lightning-fast searches.
- **LLM**: HuggingFace Hub powered by Mistral-7B-Instruct-v0.3, quantized and GPU-accelerated via Torch for superior inference speed.
- **UI**: Jupyter/ipywidgets for a polished, user-centric experience.
- **Hardware**: Optimized for CUDA-enabled environments (e.g., NVIDIA L4) to deliver efficient, scalable performance.

## Project Workflow

1. **Data Loading**: Seamlessly download the Kaggle dataset (CSV), convert to JSON, and vectorize sensor logs with LangChain and advanced embeddings.
2. **NLP Processing**: Extract key entities from user inputs using spaCy to refine and enrich queries.
3. **RAG Retrieval**: Retrieve highly relevant log contexts from the vector store for precise, data-driven analysis.
4. **LLM Inference**: Harness Mistral-7B to produce expert predictions, incorporating built-in constraints for actionable intelligence.
5. **UI Interaction**: Enable users to input logs through an interactive widget, yielding structured, professional-grade responses covering predictions, actions, costs, and urgency.

[Demo Screenshot]()
