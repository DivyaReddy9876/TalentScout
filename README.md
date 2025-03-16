# 🚀 TalentScout - AI Hiring Assistant  

## 📌 Project Overview  
TalentScout is an **AI-powered Hiring Assistant** designed to automate and enhance the candidate screening process. Using **Google's Gemini AI (LLM)**, it dynamically generates **technical interview questions** based on the applicant’s role, experience level, and tech stack. The chatbot allows applicants to enter their details, generate **AI-driven** interview questions, submit responses, and experience an **interactive hiring process** via a **Gradio UI**.  

## 🛠 Installation Instructions  
### 1️⃣ Clone the Repository  
```sh
git clone https://github.com/your-username/TalentScout-AI-Hiring-Assistant.git  
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
Replace "your_api_key" inside the script:

python
Copy
Edit
GENAI_API_KEY = "your_api_key"  # Replace with actual Google Gemini API key  
5️⃣ Run the Application
sh
Copy
Edit
python app.py  
This launches the Gradio UI, allowing users to interact with the chatbot.

📖 Usage Guide
Open the Application: Run the script to start the Gradio UI.
Enter Personal & Educational Details: Provide name, email, phone, graduation details, experience, and tech stack.
Select Job Role: Options include AI/ML Intern, SDE Intern, QA Tester, Full Stack Developer, Project Manager, Business Development Associate (BDA), etc.
Generate Technical Questions: Click "🔍 Generate Questions" to receive 5 AI-generated interview questions. If AI fails, predefined fallback questions will be used. Additional questions include:
Describe your previous experience in this field (if any).
Why are you interested in this role?
Submit Your Answers: Fill in responses and click "✅ Submit Application". A confirmation message appears: "Thank you for your responses! If you are shortlisted, our hiring team will contact you soon."
🏗 Technical Details
🔹 Tech Stack & Libraries
Python 🐍 - Core programming language
Gradio 🎨 - Interactive UI framework
Google Generative AI (Gemini API) 🤖 - AI-driven question generation
Predefined Question Database 📋 - Fallback questions
🔹 Functionality
User Input Handling: Collects candidate details via Gradio forms
AI Question Generation: Uses Google Gemini API for role-based interview questions
Fallback Mechanism: Predefined questions are used if AI fails
Final Submission: Candidate responses are stored and displayed
🎯 Prompt Design
To generate high-quality, role-specific interview questions, we use this optimized prompt:

txt
Copy
Edit
You are an interviewer preparing a technical interview for a {Fresher/Experienced} candidate applying for {Role}.  
The candidate has the following tech skills: {Tech Stack}.  
Generate 5 **technical** interview questions that are role-specific and relevant to their experience level.  
Questions should be **clear, challenging, and related to real-world applications**.  
This ensures relevance, customization, and diverse question types.

⚠ Challenges & Solutions
🔴 AI Question Generation Fails Sometimes
Issue: API fails due to network issues or rate limits.
✅ Solution: Implemented predefined fallback questions per role.

🔴 Maintaining Context & Flow
Issue: AI-generated questions needed coherence.
✅ Solution: Refined prompt engineering and used temperature=0.5.

🔴 Handling User Input Issues
Issue: Some fields (e.g., gender, graduation year) were disabled.
✅ Solution: Fixed Gradio UI to ensure all fields are editable.

🌟 Future Enhancements
🔹 Resume Parsing: Extract details from uploaded resumes.
🔹 AI-Powered Answer Evaluation: Score candidate responses using NLP.
🔹 Integration with ATS (Applicant Tracking System).
