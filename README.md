# TalentScout
# 🚀 TalentScout - AI Hiring Assistant  

## 📌 **Project Overview**  
TalentScout is an **AI-powered Hiring Assistant** designed to **automate and enhance** the candidate screening process. Using **Google's Gemini AI (LLM)**, it dynamically generates **technical interview questions** based on the applicant’s role, experience level, and tech stack.  

The chatbot allows applicants to:  
✅ Enter personal & educational details.  
✅ Generate **AI-driven** interview questions tailored to their profile.  
✅ Answer and submit responses for further review.  
✅ Provide a **smooth, interactive** hiring experience via a **Gradio**-powered UI.  

---

## 🛠 **Installation Instructions**  
Follow these steps to **set up and run** the TalentScout Hiring Assistant **locally**:

### **1️⃣ Clone the Repository**  
```sh
git clone https://github.com/your-username/TalentScout-AI-Hiring-Assistant.git
cd TalentScout-AI-Hiring-Assistant
2️⃣ Create a Virtual Environment (Optional but Recommended)
sh
Copy
Edit
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate  # On Windows
3️⃣ Install Dependencies
sh
Copy
Edit
pip install -r requirements.txt
4️⃣ Set Up the Google Gemini API Key
Replace "your_api_key" with your actual API key in the GENAI_API_KEY variable inside the script:

python
Copy
Edit
GENAI_API_KEY = "your_api_key"  # Replace with your actual Google Gemini API key
5️⃣ Run the Application
sh
Copy
Edit
python app.py
This will launch the Gradio web interface where users can interact with the chatbot.

📖 Usage Guide
Open the Application:

After running the script, a Gradio UI will open in your web browser.
Fill in Personal & Educational Details:

Provide your name, email, phone, graduation details, experience level, and tech stack.
Select Desired Job Role:

Options include AI/ML Intern, SDE Intern, QA Tester, Full Stack Developer, Project Manager, Business Development Associate (BDA), etc.
Generate Technical Questions:

Click on the "🔍 Generate Questions" button to receive 5 AI-generated technical questions based on your role and experience.
If the API fails, predefined fallback questions will be used.
Additional questions include:
Describe your previous experience in this field (if any).
Why are you interested in this role?
Submit Your Answers:

Provide answers in the designated fields.
Click on ✅ Submit Application.
A confirmation message will appear:
"Thank you for your responses! If you are shortlisted, our hiring team will contact you soon."
🏗 Technical Details
🔹 Tech Stack & Libraries Used
Python 🐍 - Core programming language.
Gradio 🎨 - Interactive UI for chatbot interaction.
Google Generative AI (Gemini API) 🤖 - LLM for AI-driven question generation.
Predefined Question Database 📋 - Backup questions if API fails.
🔹 Architecture & Functionality
User Input Handling: Collects candidate details through Gradio form fields.
AI Question Generation: Uses Google Gemini API to dynamically create role-specific technical questions.
Fallback Mechanism: If the API request fails, predefined questions are used.
Final Submission: Candidate responses are stored and displayed.
🎯 Prompt Design
To generate high-quality, role-specific interview questions, we designed optimized prompts:

txt
Copy
Edit
You are an interviewer preparing a technical interview for a {Fresher/Experienced} candidate applying for {Role}.  
The candidate has the following tech skills: {Tech Stack}.  
Generate 5 **technical** interview questions that are role-specific and relevant to their experience level.  
Questions should be **clear, challenging, and related to real-world applications**.
This prompt ensures: ✅ Relevance to the job role.
✅ Customization based on experience level.
✅ Diverse question types (conceptual, practical, and scenario-based).

⚠ Challenges & Solutions
🔴 1. AI Question Generation Fails Sometimes
Issue: Gemini API occasionally fails to return questions due to network/API limits.
✅ Solution: Implemented predefined fallback questions for each role.

🔴 2. Maintaining Context & Flow
Issue: AI-generated questions needed to be coherent and well-structured.
✅ Solution: Refined the prompt and used temperature tuning (temperature=0.5) for balanced randomness.

🔴 3. Handling User Inputs Properly
Issue: Some fields (e.g., gender, graduation year) were disabled unexpectedly.
✅ Solution: Debugged Gradio UI elements to ensure all fields are editable and user-friendly.

🌟 Future Enhancements
🔹 Resume Parsing: Extract candidate details from uploaded resumes.
🔹 AI-Powered Answer Evaluation: Score candidate responses using NLP techniques.
🔹 Integration with ATS (Applicant Tracking System) for seamless recruitment.
