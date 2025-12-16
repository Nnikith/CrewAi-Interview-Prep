# Job Interview Preparation AI Agent

An AI-powered interview preparation assistant built with **CrewAI** and **OpenAI models**, designed to generate interview questions and provide coaching-style feedback. The project is implemented as an interactive **Jupyter Notebook**, making it easy to experiment, customize roles, and iterate quickly.

---

## 🚀 Overview

This project simulates a multi-agent interview preparation workflow:

* One agent generates role-specific interview questions
* Another agent evaluates responses and provides constructive feedback
* Tasks are executed sequentially with memory enabled for contextual continuity

It is ideal for **students, job seekers, and professionals** preparing for technical, behavioral, or role-specific interviews.

---

## 📂 Project Structure

```
├── Job_Interview_Prep.ipynb   # Main Jupyter Notebook
├── README.md                 # Project documentation
├── .gitignore                # Git ignore rules
└── .env                      # Environment variables (not committed)
```

---

## 🛠️ Technologies Used

* **Python 3.9+**
* **Jupyter Notebook / JupyterLab**
* **CrewAI** (multi-agent orchestration)
* **LangChain** (OpenAI integration)
* **OpenAI API**
* **python-dotenv** (environment variable management)

---

## ✅ Prerequisites

Ensure you have the following installed:

* Python 3.9 or higher
* Jupyter Notebook or JupyterLab
* An active OpenAI API key

---

## ⚙️ Environment Setup

### 1. Create a virtual environment (recommended)

```bash
python -m venv venv
```

Activate it:

**Mac / Linux**

```bash
source venv/bin/activate
```

**Windows**

```bash
venv\Scripts\activate
```

---

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 API Key Configuration

Create a `.env` file in the project root directory:

```txt
OpenAI_CrewAI_Key=your_openai_api_key_here
```

> ⚠️ **Do not commit the `.env` file to GitHub**. It is intentionally excluded via `.gitignore`.

---

## 🧠 How the Notebook Works

### 1. Initialization

* Imports required libraries
* Loads environment variables using `python-dotenv`
* Initializes the OpenAI model

---

### 2. AI Agents

Each agent is defined with:

* **Role** – what the agent does
* **Goal** – the expected outcome
* **Backstory** – context to improve reasoning quality

Example agents:

* Interview Preparation Agent
* Coaching & Feedback Agent

---

### 3. Tasks

Tasks define the responsibilities of each agent, such as:

* Generating interview questions
* Reviewing and improving candidate answers

Tasks are executed **sequentially** to maintain logical flow.

---

### 4. Crew Execution

Agents and tasks are combined into a `Crew` object with:

* Sequential processing
* Memory enabled
* Verbose logging

Execution is started with:

```python
crew.kickoff()
```

---

### 5. Output

* Results are rendered directly in the notebook
* Uses Markdown formatting for clarity and readability

---

## ▶️ How to Run the Project

1. Launch Jupyter Notebook:

```bash
jupyter notebook Job_Interview_Prep.ipynb
```

2. Run all cells from top to bottom
3. Review the generated interview questions and coaching feedback

---

## ⭐ Best Practices Followed

* Secure handling of API keys using environment variables
* Clear separation of setup, agents, and execution logic
* Reproducible and readable notebook structure
* Git version control with clean commit history

---

## 🔮 Future Enhancements

* Role-specific interview modes (Data Analyst, Data Engineer, Product Manager, etc.)
* Persist interview results to files or a database
* Refactor notebook logic into reusable Python modules
* Expose functionality through a FastAPI backend
* Add UI integration (Streamlit or Gradio)

---

## 👤 Author

**Neelisetty Nikith**

---

## 📄 License

This project is intended for **educational and personal use**.
