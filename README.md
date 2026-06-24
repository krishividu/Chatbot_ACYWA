# Australian Child and Youth Wellbeing Atlas (ACYWA) Chatbot

## Overview

The Australian Child and Youth Wellbeing Atlas (ACYWA) Chatbot is an AI-powered conversational assistant developed to improve user navigation and accessibility within the ACYWA platform.

The chatbot helps users locate relevant datasets, understand platform terminology, apply filters, navigate Atlas maps, and access supporting resources such as user guides and metadata documents.

This project was developed as part of the CITS5553 Industry Project at The University of Western Australia.

---

## Problem Statement

The ACYWA platform contains more than 500 datasets related to child and youth wellbeing across Australia. While valuable, the platform can be difficult for users to navigate due to:

* Complex filtering options
* Technical terminology
* Multiple navigation paths
* Low digital literacy among some users

This project aims to provide a conversational interface that simplifies navigation and improves user engagement.

---

## Key Features

* Conversational AI chatbot
* Context-aware responses
* Navigation assistance for Atlas maps
* URL generation for relevant resources
* Follow-up topic suggestions
* Chat history management
* User onboarding support
* Knowledge Graph-powered information retrieval
* Retrieval-Augmented Generation (RAG)
* Real-time interaction through a web interface

---

## System Architecture

The project consists of:

### Frontend

* HTML
* CSS
* JavaScript

### Backend

* Python
* Flask
* LangChain
* OpenAI GPT-4o Mini

### Knowledge Management

* Chroma Vector Database
* Neo4j Knowledge Graph

### Deployment

* Render Cloud Platform

---

## Development Approaches

### 1. Basic Retrieval Chatbot

A simple retrieval-based system using vector embeddings stored in ChromaDB.

### 2. RAG-Based Chatbot

Implemented Retrieval-Augmented Generation using LangChain retrieval chains and conversation history.

### 3. Knowledge Graph Chatbot

Implemented Neo4j knowledge graphs to model:

* Themes
* Subthemes
* Responses

This approach achieved the best performance in terms of response accuracy and speed.

---

## Technologies Used

| Category        | Technologies                      |
| --------------- | --------------------------------- |
| Programming     | Python, JavaScript                |
| Backend         | Flask, LangChain                  |
| Frontend        | HTML, CSS, JavaScript             |
| LLM             | OpenAI GPT-4o Mini                |
| Vector Store    | ChromaDB                          |
| Knowledge Graph | Neo4j                             |
| Deployment      | Render                            |
| Evaluation      | BLEU, METEOR, ROUGE-L, SBERT, WMD |

---

## Installation

### Clone Repository

```bash
git clone https://github.com/krishni1990/acywa-chatbot.git

cd acywa-chatbot
```

### Create Environment

```bash
conda env create -f cits5553-2024.yml
conda activate acywa-chatbot
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create a `.env` file:

```env
OPENAI_API_KEY=your_api_key
```


---

## Running the Application

```bash
python app.py
```

---

## Evaluation Results

| Model           | METEOR | BLEU | ROUGE-L | SBERT | Avg Response Time |
| --------------- | ------ | ---- | ------- | ----- | ----------------- |
| Basic Retrieval | 0.43   | 0.12 | 0.34    | 0.71  | 3.89s             |
| RAG-Based       | 0.48   | 0.21 | 0.44    | 0.72  | 8.44s             |
| Knowledge Graph | 0.79   | 0.75 | 0.81    | 0.89  | 2.03s             |

The Knowledge Graph model achieved the highest overall performance.

---

## Acknowledgements

Special thanks to:

* Australian Child and Youth Wellbeing Atlas (ACYWA)
* Project supervisors and industry stakeholders

---

## License

This project was developed for academic purposes as part of CITS5553 Industry Project at The University of Western Australia.

