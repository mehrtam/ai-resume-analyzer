AI Resume Analyzer
An intelligent web application that uses a large language model to analyze and extract key information from a PDF resume. The application securely stores the extracted skills and projects in a user-specific cloud database, demonstrating a full-stack approach to a practical data-processing problem.

Features
PDF Parsing: Extracts raw text from any PDF resume.

AI-Powered Extraction: Utilizes a large language model to intelligently identify and structure skills and projects from unstructured text.

Secure Cloud Storage: Persists user-specific data in a secure Firebase Firestore database.

User-Specific Profiles: Automatically creates and manages a private profile for each user to save their resume data.

Persistent Data: Users can revisit the application at any time to view their previously saved data.

Professional and Responsive UI: The application's clean design is built with Tailwind CSS and works flawlessly on both desktop and mobile devices.

Technologies Used
Frontend: HTML, JavaScript, and Tailwind CSS for a modern, responsive user interface.

AI Model: Google's Gemini API for powerful text extraction and data structuring.

Database: Firebase Firestore for secure, scalable, and real-time data storage.

PDF Processing: PDF.js library for client-side PDF text extraction.

How to Run
Clone the repository:

git clone [https://github.com/mehrtam/ai-resume-analyzer.git](https://github.com/mehrtam/ai-resume-analyzer.git)

Navigate to the project directory:

cd ai-resume-analyzer

Open the file:
Open resume_extractor.html directly in your preferred web browser. The application is entirely self-contained within this single file, making it easy to run. No local server is required.

How it Works
The application follows a simple, yet powerful, workflow:

File Upload: A user uploads a PDF file via the clean UI.

Text Extraction: The JavaScript and PDF.js libraries work together to extract all the text content from the PDF on the client-side.

AI Analysis: The extracted text is sent to the Gemini API with a specific prompt to identify and format skills and projects into a structured JSON object.

Data Persistence: The returned JSON data is saved to a secure document in a Firestore database. A unique user ID is used to ensure that data remains private to each user.

Data Display: The extracted data is then displayed in the text areas, and is automatically loaded from Firestore on subsequent visits.

Where is the data saved?
Data is saved to a secure, private document in the Firebase Firestore cloud database. It is stored within a collection that is uniquely identified by the user's ID, ensuring that only the user who uploaded the resume can access their data.

The full path to the data is:

artifacts/{your_app_id}/users/{your_user_id}/resumes

This structure prevents unauthorized access and showcases a strong understanding of database security principles.
