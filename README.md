**🧠 Smart Task Planner (AI-Powered Goal Breakdown)**


  The Smart Task Planner is a single-page web application designed to break down ambitious, high-level user goals into structured, actionable, and logically sequenced project tasks using advanced LLM reasoning.
  This project was developed for the purpose of demonstrating key capabilities in AI integration, structured data generation, and responsive frontend design, fulfilling the core objective of generating actionable tasks with timelines using AI.

  
**✨ Features**

  
  •	AI Reasoning: Uses the Google Gemini API (gemini-2.5-flash-preview-05-20) to act as a virtual project manager, providing intelligent task breakdown, timeline estimations, and dependency mapping.
  •	Structured Output: Enforces a strict JSON Schema in the LLM output, ensuring reliable data extraction for taskName, timelineDays (numeric), and dependencies.
  •	Real-Time Generation: Provides a smooth user experience with loading indicators and error handling (including exponential backoff for robust API communication).
  •	Local History Management: Stores all generated plans and original goals locally using localStorage, allowing users to review and delete past plans.
  •	Responsive Design: Built using HTML and Tailwind CSS for a modern, mobile-friendly interface.

  
**🚀 Technical Stack**


  •	Frontend: HTML5, CSS (Tailwind CSS via CDN), JavaScript (ES6+)
  •	LLM Backend: Gemini API (gemini-2.5-flash-preview-05-20)
  •	Persistence: Browser localStorage for history.

  
**🛠️ Setup and Installation**


  Since this is a single-file application, setup is simple:
  1.	Obtain a Gemini API Key: Get a key from Google AI Studio.
  2.	Clone the Repository:
  3.	git clone [Your-GitHub-Repo-URL]
  4.	cd smart-task-planner
  
  5.	Configure API Key: Open the index.html file in a text editor and locate the following line around the start of the <script> block:
  6.	const API_KEY = "AIzaSyBSmP8QGNLPX8nfb0XoVK83dhMvxTd81EI"; 
  
  Replace the placeholder value with your actual Gemini API Key.
  7.	Run Locally: Double-click the index.html file, or for best results (and future API integrations), run it using a local development server (e.g., VS Code's "Live Server" extension).

  
**💡 Code Highlights**


  The primary innovation lies in the JavaScript logic that manages the LLM call:
  1.	System Prompt (SYSTEM_PROMPT): Defines the persona of the AI (expert project manager) to ensure high-quality, professional task logic.
  2.	Response Schema (RESPONSE_SCHEMA): Crucial for development—this object enforces the JSON format, guaranteeing that the output is parsable and contains the required timelineDays and dependencies fields.
  3.	Error Handling (Exponential Backoff): The generatePlan() function implements retry logic with increasing delays (currentDelay *= 2) to handle transient network issues and ensure reliable API calls.
  4.	Local Persistence: The savePlanLocally() and getStoredPlans() functions manage the history feature using localStorage.
**Developed by Ashutosh Khatuwala (22BCI0029)**

