# LangChain LCEL Chains Guide

A clean, beginner-friendly guide demonstrating how to build and orchestrate LLM workflows using **LangChain Expression Language (LCEL)**.

---

## 📌 What's Inside?

This repository covers 4 essential types of chains in LangChain:

1. **Simple Chain (`simple_chain.py`)**
   - Connects a Prompt, Model, and Output Parser in a straight line (`prompt | model | parser`).
   - Example: Generates 5 interesting facts on any topic.

2. **Sequential Chain (`sequential_chain.py`)**
   - Passes the output of one chain directly into the next prompt.
   - Example: Generates a detailed report on a topic and automatically condenses it into a 5-line summary.

3. **Parallel Chain (`parallel_chain.py`)**
   - Runs multiple tasks simultaneously using `RunnableParallel`.
   - Combines multiple LLMs (OpenAI + Google Gemini).
   - Example: Takes a text snippet, generates summary notes and a 5-question quiz simultaneously, then merges them into a single study guide.

4. **Conditional Chain (`conditional_chain.py`)**
   - Routes flow dynamically based on output values using `RunnableBranch`.
   - Uses Pydantic for structured output classification (`Feedback`).
   - Example: Classifies customer feedback as positive or negative and triggers the appropriate response.

---

## 🚀 Quick Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/langchain-chains.git
cd langchain-chains
```

### 2. Create and activate a virtual environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure API Keys
Create a `.env` file in the root directory (you can copy `.env.example`):
```env
OPENAI_API_KEY="your-openai-api-key"
GOOGLE_API_KEY="your-google-api-key"
```

---

## 💻 Running the Examples

Run any chain script directly with Python:

```bash
# 1. Simple chain
python simple_chain.py

# 2. Sequential chain
python sequential_chain.py

# 3. Parallel chain (multi-model)
python parallel_chain.py

# 4. Conditional chain (branching)
python conditional_chain.py
```

Each script also prints an ASCII graph of its runnable pipeline to help visualize the flow.

---

## 🛠️ Tech Stack
- **LangChain & LCEL**
- **OpenAI & Google Gemini**
- **Pydantic**
