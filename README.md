TalentScout - AI Hiring Assistant

🚀 Project Overview

TalentScout is an AI-powered Hiring Assistant designed to automate and enhance the candidate screening process. Using Google's Gemini AI (LLM), it dynamically generates technical interview questions based on the applicant’s role, experience level, and tech stack. The chatbot allows applicants to enter their details, generate AI-driven interview questions, submit responses, and experience an interactive hiring process via a Gradio UI.

🛠 Installation Instructions

1️⃣ Clone the Repository

git clone https://github.com/DivyaReddy9876/TalentScout
cd TalentScout-AI-Hiring-Assistant

2️⃣ Create a Virtual Environment (Optional)

# macOS/Linux
python -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
venv\Scripts\activate

3️⃣ Install Dependencies

pip install -r requirements.txt

🎯 Usage Guide

Running the Application

python app.py

This will start the chatbot interface in a web browser using Gradio.

💡 Features

🤖 AI-powered Chatbot for initial candidate screening

📝 Dynamic Question Generation based on Tech Stack

📄 Gradio UI for an interactive experience

🔄 Context Handling for seamless conversations

🚀 Easy Deployment on cloud platforms

🏗 Architecture

graph TD;
  User-->GradioUI;
  GradioUI-->Backend(Python);
  Backend-->GeminiAI;
  GeminiAI-->Response;
  Response-->GradioUI;

🧩 Code Snippets

📌 Main App (app.py)

import gradio as gr
import google.generativeai as genai

genai.configure(api_key="YOUR_GEMINI_API_KEY")

def generate_questions(name, experience, position, tech_stack):
    prompt = f"""Generate 3-5 technical questions for a candidate applying for {position} with {experience} years of experience in {tech_stack}."""
    response = genai.generate_text(prompt)
    return response['text']

demo = gr.Interface(
    fn=generate_questions,
    inputs=["text", "text", "text", "text"],
    outputs="text",
    title="TalentScout AI - Hiring Assistant"
)

demo.launch()

📌 Example Prompt Engineering

prompt = f"""You are an AI Hiring Assistant. Based on the given tech stack, generate relevant technical interview questions.
Tech Stack: Python, Django, PostgreSQL
Experience: 3 years
Position: Backend Developer
"""

🔧 Deployment

Deploy on Hugging Face Spaces

Create a new Space in Hugging Face

Select Gradio as the interface

Upload your files & add a requirements.txt

Deploy and get a live demo link!
