# FuturePath - AI Career Guidance & Assessment Platform (React + Redux Toolkit)

A web application converted from vanilla HTML/CSS/JavaScript into a modern, reactive single-page application using **React 18**, **Redux Toolkit (RTK)**, and **React Router DOM**.

---

## 🚀 Key Features

1. **State Management with Redux Toolkit (`@reduxjs/toolkit`)**:
   - `authSlice`: Handles user authentication state, registration with academic parameters (degree stream, college, year, semester), demo login, profile editing, and persistence with `localStorage`.
   - `assessmentSlice`: Orchestrates live Aptitude and Course-Specific Technical tests, real-time countdown timers, question navigation, scoring algorithms, and review of incorrect answers.
   - `careerSlice`: Manages target career selection, milestone checklist progress, dynamic readiness scoring, course enrollments, internships, and job applications.
   - `uiSlice`: Controls theme switching (Dark & Light modes), responsive sidebar visibility, and notifications.

2. **Full Page & Feature Conversion**:
   - **Landing Page (`/`)**: Hero banner with live career progress metrics, feature cards, and career transformation steps.
   - **Authentication (`/login`, `/signup`)**: Form validation with regex, password security criteria (uppercase + digit + min 6 chars), phone number formatting, and demo credentials.
   - **Main Dashboard (`/dashboard`)**: Unified academic summary, live aptitude & technical assessment scores, target career readiness meter, interactive roadmap milestone tracker, and quick tools.
   - **Assessments Hub (`/assessments`)**: Stream-tailored technical and cognitive aptitude assessment selection.
   - **Live Aptitude Test (`/assessments/aptitude`)**: 10 randomized questions, real-time countdown timer (10 mins), category tags, selected answer feedback, and auto-submission.
   - **Aptitude Results (`/assessments/aptitude/result`)**: Score / 100, correct vs. wrong breakdown, confetti celebration, and mistake reviews with detailed explanations.
   - **Live Technical Test (`/assessments/technical`)**: Domain questions customized to the student's degree (CSE, AIML, ECE, MECHANICAL, CIVIL), countdown timer (15 mins), and category badges.
   - **Technical Results (`/assessments/technical/result`)**: Comprehensive report with technical explanations for every question.
   - **My Profile (`/profile`)**: Personal details, academic degree selector, skills management, and in-place profile updates.
   - **Courses (`/courses`)**: Catalog with filters, syllabus metrics, progress tracking, and enroll buttons.
   - **Career Recommendations (`/career-recommendations`)**: AI career guidance with salary packages, market demand, and prerequisite skills.
   - **Skill Gap Analysis (`/skill-gap`)**: Direct competency comparison against industry expectations.
   - **Learning Roadmap (`/roadmap`)**: Interactive milestone checklist that recalculates career readiness upon completion.
   - **Internships & Jobs (`/internships`, `/jobs`)**: Curated opportunities matching the student's degree.
   - **Resume Builder (`/resume-builder`)**: ATS-compatible resume generator populated with verified FuturePath assessment scores.
   - **Achievements (`/achievements`)**: Unlockable badges based on test completions, score thresholds, and milestones.
   - **Settings (`/settings`)**: Theme switch (Light / Dark mode), profile summary, data export (`FuturePath_Data.json`), and logout.

3. **🚀 5 Fresh Innovation Features**:
   - **🕵️ Career Reality Checker (`/career-reality-checker`)**: Shows unvarnished day-in-the-life schedules, myth vs reality cards, must-have technical/soft competencies, first 90-day responsibilities, actual tough interview gotchas, and an interactive live readiness checklist saved to `localStorage`.
   - **🧑💻 GitHub Project Analyzer (`/github-analyzer`)**: Connects real GitHub repositories via GitHub's public REST API to audit documentation health (0-100 score), break down language bytes, detect demonstrated engineering skills, evaluate target career alignment %, suggest fixes, and recommend next portfolio projects.
   - **🎯 Career What-If Simulator (`/what-if-simulator`)**: Interactive skill sandbox allowing students to test scenarios like *"What if I learn Python and SQL?"*, instantly seeing unlocked careers, transferable skill maps between roles, and comparative salary/work-life benchmarks.
   - **🧠 Personal Weakness Detector (`/weakness-detector`)**: Isolates granular sub-topics (OOP, Loops, Relational DBMS, Networking, Quant Percentages) where the student loses marks in assessments, provides root-cause explanations, curated study guides, and instant 3-question micro-drills to upgrade mastery on the spot.
   - **🏢 Company-Specific Placement Prep (`/company-prep`)**: Comprehensive placement preparation hub for TCS, Infosys, Capgemini, Amazon, and more. Features verified recruitment stages, technical interview Q&As with model answers, exam patterns, coding patterns, resume checklists, and timed mock placement tests!

---

## 🛠️ Technology Stack

- **Framework**: React 18
- **State Management**: Redux Toolkit (RTK) & React-Redux
- **Routing**: React Router DOM (v6)
- **Icons**: Lucide React
- **Build Tool**: Vite
- **Visual Effects**: Canvas Confetti
- **Styling**: Modern CSS Custom Properties with full Dark / Light mode support

---

## 🏃 Running the Application

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start the development server**:
   ```bash
   npm run dev
   ```
   Open `http://localhost:3000` (or the port indicated by Vite) in your browser.

3. **Build for production**:
   ```bash
   npm run build
   ```

4. **Preview the production build**:
   ```bash
   npm run preview
   ```

---

## 📁 Project Structure

```
├── legacy-vanilla/            # Preserved backup of original vanilla code
├── public/                    # Static assets
├── src/
│   ├── components/            # Reusable UI components (Sidebar, Header, Navbar, AppLayout, ProtectedRoute)
│   ├── data/                  # Normalized datasets (Aptitude & Technical question banks, Courses, Careers, Jobs)
│   ├── pages/                 # Full application pages
│   ├── store/
│   │   ├── slices/            # Redux Toolkit slices (auth, assessment, career, ui)
│   │   └── index.js           # Redux configureStore
│   ├── App.jsx                # Router configuration & Theme provider
│   ├── index.css              # Design system & CSS variables
│   └── main.jsx               # Application entrypoint
├── index.html                 # Vite HTML root
├── package.json
└── vite.config.js
```
