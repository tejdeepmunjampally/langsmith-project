🚀 LangSmith Tracing with Gemini & LangChain

This project demonstrates how to integrate LangSmith, LangChain, and Google Gemini to monitor, trace, and evaluate LLM applications.

📌 Overview

The notebook covers:

Setting up LangSmith for observability
Configuring Google Gemini API access
Building simple LangChain workflows
Enabling tracing for prompt executions
Monitoring chain runs inside LangSmith
🛠️ Tech Stack
Python
LangChain
LangSmith
Google Gemini (Gemini 2.5 Flash)
📂 Project Structure
.
├── task_6_langsmith.ipynb
└── README.md
⚙️ Installation

Install the required dependencies:

pip install langchain_openai
pip install langchain_google_genai
pip install --upgrade langchain_google_genai
pip install langsmith
🔑 Environment Setup

Configure the following API keys:

LANGSMITH_API_KEY
GOOGLE_API_KEY

Enable LangSmith tracing:

os.environ["LANGSMITH_TRACING"] = "true"
os.environ["LANGSMITH_PROJECT"] = "my-langchain-project"
🤖 Initialize Gemini Model
from langchain_google_genai import ChatGoogleGenerativeAI

llm = ChatGoogleGenerativeAI(
    model="gemini-2.5-flash"
)
🧠 Create a Prompt Chain
from langchain_core.prompts import ChatPromptTemplate

prompt = ChatPromptTemplate.from_template(
    "Tell me a brief {style} joke about {topic}."
)

chain = prompt | model
▶️ Run the Chain
response = chain.invoke({
    "style": "funny",
    "topic": "AI"
})

print(response.content)
📊 LangSmith Monitoring

All executions are automatically traced and can be viewed in LangSmith.

Features:

Prompt Tracking
Latency Monitoring
Input/Output Inspection
Debugging LLM Applications
Performance Evaluation
🎯 Learning Outcomes

After completing this project, you will understand:

LangSmith observability workflows
LangChain chain creation
Gemini model integration
Prompt tracing and debugging
LLM application monitoring
📸 Sample Use Cases
AI Chatbots
Agentic AI Systems
Prompt Engineering
LLM Evaluation
Production Monitoring
👨‍💻 Author

Tejdeep Munjampally

B.Tech Student | AI & Software Engineering Enthusiast

GitHub: https://github.com/tejdeepmunjampally
