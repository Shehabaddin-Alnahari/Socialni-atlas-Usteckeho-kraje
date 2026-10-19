# 📊 Sociální Atlas Ústeckého Kraje (Social Atlas of the Ústí Region)

> **Note:** This repository is a fork of a team project developed during a 24-hour Open Data Hackathon. 

## 🎯 About the Project
The goal of this project was to create an interactive web dashboard for analyzing regional social and economic data (such as unemployment rates) in the Ústí Region. It consists of a FastAPI backend that processes open government data and a Streamlit frontend for data visualization.

## 👨‍💻 My Contributions
Due to the strict 24-hour time limit, we heavily leveraged AI tools (Claude) for rapid code generation. My primary role within the team involved:
* **Project Coordination & Rapid Prototyping:** Managed the workflow and integrated AI-generated code to accelerate the development of the MVP (Minimum Viable Product).
* **Frontend & Visualization Setup:** Collaborated on configuring the **Streamlit** dashboard and adjusting the data visualization templates for regional unemployment statistics.

---
title: Socialni Atlas Usteckeho Kraje
emoji: 📊
colorFrom: blue
colorTo: green
sdk: streamlit
app_file: social_atlas/app.py
pinned: false
---

# 🚀 Local Development Setup

We are using Docker to run the entire project environment locally. This ensures that both the FastAPI backend and Streamlit frontend work perfectly together on everyone's machine without Python version conflicts.

## Prerequisites
Make sure you have modern Docker installed and running on your machine:
- **Windows / Mac:** Install and open [Docker Desktop](https://www.docker.com/products/docker-desktop)
- **Linux:** Install Docker Engine and the Compose plugin.

## 🛠️ How to Run the Project

1. Open your terminal and navigate to the root folder of this project.
2. Run the following command to build and start both services:

   docker compose up --build

3. Once the terminal shows that both services are running, open your browser:
   - **Frontend (Dashboard):** http://localhost:8501
   - **Backend (API):** http://localhost:8000

*Note: The backend API takes a few seconds to fully boot up because it caches the massive 100MB government dataset into memory on startup. You will see a log in the terminal when it finishes loading.*

## 🛑 How to Stop the Project

To stop the servers, simply press `Ctrl + C` in your terminal. 
If you want to fully remove the containers and clean up your system, run:

   docker compose down
