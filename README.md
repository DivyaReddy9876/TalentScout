🚀 TalentScout - AI Hiring Assistant
📌 Project Overview
TalentScout is an AI-powered Hiring Assistant designed to automate and enhance the candidate screening process.

🔹 Uses Google's Gemini AI (LLM) for dynamic question generation
🔹 Generates role-specific technical questions based on experience & tech stack
🔹 Fallback mechanism for predefined questions if AI fails
🔹 Provides a smooth and interactive hiring experience via Gradio UI

⚙️ Installation Instructions
1️⃣ Clone the Repository
sh
Copy
Edit
https://github.com/DivyaReddy9876/TalentScout
cd TalentScout-AI-Hiring-Assistant  
2️⃣ Create a Virtual Environment (Optional)
sh
Copy
Edit
python -m venv venv  
source venv/bin/activate  # macOS/Linux  
venv\Scripts\activate  # Windows  
3️⃣ Install Dependencies
sh
Copy
Edit
pip install -r requirements.txt  
4️⃣ Set Up the Google Gemini API Key
Replace "your_api_key" in app.py:

python
Copy
Edit
GENAI_API_KEY = "your_api_key"  # Replace with your actual Google Gemini API key  
5️⃣ Run the Application
sh
Copy
Edit
python app.py  
✅ This launches the Gradio UI, allowing users to interact with the chatbot.

🖥️ Usage Guide
1️⃣ Start the Application by running app.py
2️⃣ Enter Personal & Academic Details in the form
3️⃣ Select Your Desired Job Role, including:

AI/ML Intern
SDE Intern / SDE Experienced
QA Tester
Full Stack Developer
Project Manager
Business Development Associate (BDA)
4️⃣ Click “🔍 Generate Questions” – AI will generate role-specific interview questions
5️⃣ Submit Your Answers & get a confirmation message
🏗 Technical Details
🔹 Tech Stack
✔ Python 🐍 – Backend Processing
✔ Gradio 🎨 – Interactive UI
✔ Google Gemini AI 🤖 – AI-driven question generation
✔ Predefined Question Database 📋 – Backup for AI failures

🔹 Core Functionalities
🔹 User Input Handling – Collects candidate details
🔹 AI Question Generation – Role & experience-based questions
🔹 Fallback System – Predefined questions if AI fails
🔹 Submission Process – Stores and processes candidate responses

🎯 Prompt Design
To generate high-quality, role-specific interview questions, we use this optimized prompt:

txt
Copy
Edit
You are an interviewer preparing a technical interview for a {Fresher/Experienced} candidate applying for {Role}.  
The candidate has the following tech skills: {Tech Stack}.  
Generate 5 **technical** interview questions that are role-specific and relevant to their experience level.  
Questions should be **clear, challenging, and related to real-world applications**.  
✅ This ensures relevance, customization, and diverse question types.

⚠️ Challenges & Solutions
Challenge	Solution
AI Question Generation Fails Sometimes	Implemented a fallback mechanism using predefined questions
Maintaining Context & Flow	Improved prompt engineering & set temperature=0.5
Handling Disabled Fields in UI	Fixed Gradio UI issues to ensure all fields are editable
🚀 Future Enhancements
✅ Resume Parsing – Extract details from uploaded resumes
✅ AI-Powered Answer Evaluation – Score candidate responses using NLP
✅ Integration with ATS (Applicant Tracking System)
