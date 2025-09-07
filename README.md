# 📄 AI Resume Analyzer  

An intelligent web application that uses a **Large Language Model (LLM)** to analyze and extract key information from PDF resumes.  
This project demonstrates a **full-stack approach** to solving a practical data-processing problem by securely storing extracted **skills** and **projects** in a user-specific cloud database.  

---

## 🚀 Features  

- **PDF Parsing** – Extracts raw text from any PDF resume on the client side.  
- **AI-Powered Extraction** – Utilizes **Google’s Gemini API** to intelligently identify and structure skills and projects.  
- **Secure Cloud Storage** – Persists user data in **Firebase Firestore** with strict security rules.  
- **User-Specific Profiles** – Each user automatically gets a private profile to store resume data.  
- **Persistent Data** – Users can revisit the app anytime to view previously saved results.  
- **Responsive UI** – Clean, professional design built with **Tailwind CSS**, optimized for desktop and mobile.  

---

## 🛠️ Technologies Used  

- **Frontend:** HTML, JavaScript, Tailwind CSS  
- **AI Model:** Google Gemini API  
- **Database:** Firebase Firestore (secure, scalable, real-time)  
- **PDF Processing:** [PDF.js](https://mozilla.github.io/pdf.js/)  

---

## 📂 Project Setup  

### 1. Clone the repository  
```bash
git clone https://github.com/mehrtam/ai-resume-analyzer.git
2. Navigate to the project folder
bash
Copy code
cd ai-resume-analyzer
3. Run the application
Simply open resume_extractor.html in your web browser.
The app is self-contained in a single HTML file — no local server required.

⚙️ How It Works
File Upload – User uploads a PDF resume via the UI.

Text Extraction – PDF.js extracts raw text from the PDF.

AI Analysis – Text is sent to Gemini API with a custom prompt to output structured JSON (skills & projects).

Data Persistence – The JSON data is securely saved in Firestore, scoped by a unique user ID.

Data Display – Results are displayed instantly and auto-loaded on future visits.

🔒 Data Security
All data is securely stored in Firebase Firestore under a user-specific path:

bash
Copy code
artifacts/{your_app_id}/users/{your_user_id}/resumes
Each resume is tied to a unique user ID, preventing unauthorized access.

This structure enforces privacy and reflects strong database security principles.
