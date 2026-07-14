# Josh Talks AI - Human Evaluation Benchmark for Text-to-Image Indian Ethnic Clothing Models

This repository contains the complete codebase and documentation for the **Josh Talks AI human evaluation benchmark**. The project compares leading text-to-image AI models—specifically **GPT Image 1**, **Gemini 2.5 Flash**, and **Gemini 2.5 Flash Preview**—on their ability to generate accurate, high-fidelity, and culturally representative Indian ethnic clothing images.

## Project Links & Deliverables
*   **GitHub Repository**: [Anjaligarg12/JoshTalk](https://github.com/Anjaligarg12/JoshTalk)
*   **Live Deployment**: [Josh Talks AI](https://josh-talk-rho.vercel.app/)
*   **Research Report (PDF)**: [Josh Talks AI – Text-to-Image Evaluation for Indian Ethnic Clothing.pdf](Josh%20Talks%20AI%20%E2%80%93%20Text-to-Image%20Evaluation%20for%20Indian%20Ethnic%20Clothing.pdf)
*   **Excel/CSV Responses File**: [AI_Image_Evaluation_Responses (1).csv](AI_Image_Evaluation_Responses%20(1).csv)
*   **Video Walkthrough Script**: [VIDEO_SCRIPT.md](VIDEO_SCRIPT.md)
*   **Submission Checklist**: [SUBMISSION_CHECKLIST.md](SUBMISSION_CHECKLIST.md)
*   **Interactive HTML Report**: [index.html](index.html)
*   **Evaluation Form Web App**: [evaluation.html](evaluation.html)
*   **Google Form Automation Script**: [create_google_form.gs](create_google_form.gs) (Google Apps Script to generate the evaluation form and response Google Sheet automatically)

---

## Features
1.  **Human Evaluation Form (`evaluation.html`)**:
    *   Side-by-side comparison interface showcasing generated clothing designs.
    *   Dimension-based scoring (Prompt Accuracy, Visual Realism, Cultural Accuracy, Fabric Details, E-commerce Readiness).
    *   Anonymized evaluation workflow (randomized Model A/B/C layouts) to eliminate bias.
2.  **Real-Time Admin Dashboard**:
    *   Live metrics sync powered by Google Firestore.
    *   Interactive charts (breakdown of scores, demographic age distribution, familiarity profiling) built with Chart.js.
    *   Administrative actions: reload seed dataset, clear data, run star diagnostics.
3.  **PDF-Ready Research Report (`index.html`)**:
    *   An A4 portrait-aligned research document.
    *   Contains the complete methodology, demographics, key insights, conclusion, scaling roadmap, and reflections.
4.  **CSV Response Exporter**:
    *   Allows admins to export collected evaluation responses to a standardized CSV/Excel format.

---

## Tech Stack
*   **Core**: HTML5, Vanilla JavaScript (ES6+).
*   **Styling**: Vanilla CSS3 (Custom design tokens, glassmorphism, responsive grid layout, A4 print layout).
*   **Database**: Google Firebase / Firestore Compat SDK (Real-time sync & state persistence).
*   **Visualization**: Chart.js (Responsive bar and pie charts).
*   **Icons**: FontAwesome 6.4.0.

---

## Firebase Setup

Follow these steps to set up Firestore for your local or production environment:

1.  **Create a Firebase Project**:
    *   Go to the [Firebase Console](https://console.firebase.google.com/).
    *   Click **Add Project** and name it (e.g., `josh-talks-ai-eval`).
2.  **Enable Firestore Database**:
    *   In the sidebar, click on **Build** -> **Firestore Database**.
    *   Click **Create Database** and select **Start in test mode** (allows reads/writes for testing).
    *   Set your Firestore Database Location (e.g., `asia-south1` or `us-central1`).
3.  **Retrieve Configuration Keys**:
    *   Navigate to Project Settings (gear icon) -> **General**.
    *   Under *Your apps*, click the web icon (`</>`) to register a web app.
    *   Copy the `firebaseConfig` object (includes API key, Auth domain, Project ID, etc.).
4.  **Add Configuration to Code**:
    *   Open `evaluation.html` and locate the Firebase configuration script block (around line 2450-2500).
    *   Paste your config keys:
        ```javascript
        const firebaseConfig = {
          apiKey: "YOUR_API_KEY",
          authDomain: "YOUR_AUTH_DOMAIN",
          projectId: "YOUR_PROJECT_ID",
          storageBucket: "YOUR_STORAGE_BUCKET",
          messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
          appId: "YOUR_APP_ID"
        };
        firebase.initializeApp(firebaseConfig);
        const db = firebase.firestore();
        ```
5.  **Initialize Database Seed Data**:
    *   Launch the app locally and click **View Dashboard**.
    *   Under *Administrative Actions*, click **Reload Seed Data** to populate Firestore with the 12 default test participant responses.

---

## Folder Structure
```directory
JoshTalk/
│
├── assets/                     # Image assets and model output images
│   ├── prompt1_gpt.jpg
│   ├── prompt1_gemini_f.jpg
│   └── ...
│
├── index.html                  # A4 print-ready Research Report
├── evaluation.html             # Human Evaluation Web App & Admin Dashboard
├── create_google_form.gs       # Google Apps Script to automate Google Form & Sheet creation
│
├── AI_Image_Evaluation_Responses (1).csv   # Exported dataset (12 participants)
│
├── README.md                   # Project documentation (this file)
├── VIDEO_SCRIPT.md             # Walkthrough video outline and script
└── SUBMISSION_CHECKLIST.md     # Final submission items checklist
```

---

## How to Run

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/Anjaligarg12/JoshTalk.git
    cd JoshTalk
    ```
2.  **Run with Local Server**:
    *   Use VS Code's **Live Server** extension, or run a python local web server:
        ```bash
        # Python 3
        python -m http.server 8000
        ```
    *   Access the evaluation page at `http://localhost:8000/evaluation.html` and the report cover at `http://localhost:8000/index.html`.
3.  **Deploying to Vercel**:
    *   Install Vercel CLI: `npm install -g vercel`.
    *   Run `vercel` in the project root directory and follow instructions to deploy.

