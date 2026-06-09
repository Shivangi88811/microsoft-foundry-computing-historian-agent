# Microsoft Foundry Computing Historian Agent

## Project Overview

This project demonstrates how to build, configure, publish, and consume an AI agent using Microsoft Foundry and Azure AI.

The agent is designed as a **Computing Historian** that answers questions about the history of computing, artificial intelligence milestones, notable computer scientists, and vintage computing systems.

This project was completed as part of **Microsoft AI Skills Fest**, happening from **June 8–12**, and extended into a local Python Flask client application using Visual Studio Code.

---

## Project Goal

The goal of this project was to understand the end-to-end lifecycle of an AI agent:

- Create a Microsoft Foundry project
- Deploy a generative AI model
- Configure agent instructions
- Add a Web Search tool
- Save the model configuration as an agent
- Test the agent in Microsoft Foundry
- Continue development in Visual Studio Code
- Call the published agent from a Python client application
- Run the agent through a local Flask web app

---

## Technologies Used

- Microsoft Foundry
- Azure AI
- Azure for Students Subscription
- GPT-4.1 Mini
- Foundry Toolkit for Visual Studio Code
- Azure CLI
- Python
- Flask
- OpenAI Responses API
- Azure Identity
- Git and GitHub
- Visual Studio Code

---

## Agent Details

### Agent Name

`computing-historian`

### Model

`gpt-4.1-mini`

### Agent Purpose

The agent provides information about:

- History of computing
- Artificial intelligence milestones
- Significant people in computing
- Notable vintage computers
- Major technology events and inventions

### System Instructions

The agent was configured to act as an expert in the history of computing and AI. It answers questions related to significant people, events, and vintage computers while avoiding unrelated topics.

### Tool Added

- Web Search

The Web Search tool allows the agent to retrieve current information when needed.

---

## Architecture

```text
User
 ↓
Flask Web Application
 ↓
Python Agent Client
 ↓
OpenAI Responses API
 ↓
Microsoft Foundry Agent Endpoint
 ↓
GPT-4.1 Mini + Web Search Tool
 ↓
Agent Response
```

---

## Project Workflow

### 1. Microsoft Foundry Project Setup

Created a Microsoft Foundry project using an Azure for Students subscription.

### 2. Model Deployment

Deployed the `gpt-4.1-mini` model inside the Foundry project.

### 3. Agent Configuration

Configured system instructions for a computing history-focused AI assistant.

### 4. Tool Integration

Added the Web Search tool to allow the agent to search external information when required.

### 5. Agent Publishing

Saved and published the agent to generate a dedicated Responses API endpoint.

### 6. Visual Studio Code Development

Used the Foundry Toolkit extension in Visual Studio Code to connect to the Foundry project and generate Python code for testing the agent.

### 7. Python Agent Testing

Created a Python script to send prompts to the agent and display responses in the terminal.

### 8. Client Application Integration

Configured a Flask-based client application to call the published agent endpoint using the OpenAI Responses API and Azure Entra ID authentication.

---

## Local Setup

### Clone the repository

```bash
git clone https://github.com/Shivangi88811/microsoft-foundry-computing-historian-agent.git
cd microsoft-foundry-computing-historian-agent
```

### Create virtual environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Configure environment variables

Create a `.env` file using `.env.example` as a reference.

```env
AGENT_ENDPOINT=your_agent_openai_protocol_endpoint_here
```

### Run the application

```bash
python app.py
```

Open the app in your browser:

```text
http://localhost:5000
```

---

## Sample Prompts Tested

- What was ENIAC?
- How does it compare with COLOSSUS?
- Tell me about the Commodore 64.
- What was Grace Hopper's contribution to computing?
- What was Alan Turing's contribution to AI?

---

## Key Learnings

- How Microsoft Foundry organizes projects, models, agents, and tools
- How to configure system instructions for an AI agent
- How to add tools such as Web Search
- How to publish an agent endpoint
- How to call a Foundry agent using Python
- How to use Azure Entra ID authentication with the OpenAI Responses API
- How to integrate an AI agent into a Flask client application
- How to document an AI agent project for GitHub and portfolio use

---

## Future Enhancements

- Add Azure AI Search with custom documents
- Add conversation logging
- Add user authentication
- Deploy the Flask application to Azure App Service
- Create a Resume Optimization Agent using the same architecture
- Add evaluation metrics for response quality

---

## Author

Shivangi Ajmeri