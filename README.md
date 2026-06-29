# 💼 WorkStudio HRMS

WorkStudio is a premium, high-fidelity Human Resource Management System (HRMS) dashboard designed for **R P Daga & Co.** It serves as a working prototype showcasing a modern, aesthetic user interface built on a custom web component runtime.

---

## ✨ Features at a Glance

WorkStudio offers a dual-experience workflow, enabling roles to switch seamlessly between **HR Admin** and **Employee** perspectives:

### 👤 HR Admin Perspective (Aarav Mehta)
*   **Organisation Overview**: Unified dashboard with live indicators, tracking Total Employees, Active Personnel, Departments, Branches, and New Joiners.
*   **Employee Directory**: Searchable directory displaying employee databases with a card/table view toggle, search bar, department-wise filtering, and detail drawers.
*   **Department Distribution**: Visual breakdown of staff across departments (Audit, Tax, Advisory, Compliance, etc.) with custom animated progress indicators.
*   **Organisation Structure**: Interactive reporting tree visualising hierarchy (Managing Partner &rarr; Department Heads).
*   **Branch & Team Administration**: Quick-glance list of active offices, staff distributions, and department leaders.
*   **Attendance & Work Tracker**: Operational tools to verify attendance reports, logs, and branch-level headcounts.
*   **Payroll & Compensation Control**: Overview of payroll reports, status tracking, and disbursement tools.

### 💼 Employee Perspective (Kabir Nair)
*   **My Workspace**: Dedicated home feed containing direct check-in actions, break states, and daily metrics.
*   **Personalised Profiles**: Comprehensive sections for Bank details, Personal info, Work History, Client engagements, and verified KYC Documents.
*   **My Leave Planner**: Leave request forms, status tracking, and breakdowns of Sick, Casual, and Earned leaves.
*   **My Payslips**: Quick access to monthly salaries, tax withholding summaries (Form 16), and bank disbursements.
*   **Document Vault**: Secured portal housing critical credentials (Aadhaar, PAN, Passport, Education Certificates) with validity alerts.

---

## 🛠️ Interactive Modules

WorkStudio is packed with micro-interactions and real-time state handlers:

1.  **Analog Live Clock & Worked-Hours Widget**
    *   An SVG-driven analog clock displaying real-time hours, minutes, and seconds.
    *   Tracks checking-in/out and breaks.
    *   Updates a persistent "Worked today" time accumulator.
2.  **Work Log / To-Do Task Tracker**
    *   Fully functional checklist allowing users to add, toggle completion, and delete tasks dynamically.
    *   Persists entries inside local browser storage.
3.  **Dynamic Profile Side-Drawer**
    *   Sliding drawer for quick-inspecting employee directory details, displaying manager reporting lines, contact information, and verification tags.
4.  **Action Forms & Modals**
    *   Pop-up modals for core actions: *Add Employee*, *Add Department*, *Add Branch*, *Apply for Leave*, *Upload Documents*, and *Edit Profile*.
5.  **State Persistence**
    *   State items like worked time, check-out statuses, and custom worklogs are saved to `localStorage` to ensure they persist across page reloads.

---

## 🚀 Tech Stack & Architecture

WorkStudio is built on a modern, decoupled Document Component (DC) design:

*   **Dynamic Component Rendering**: Utilises a proprietary custom tag system (`<x-dc>`) parsed and booted at runtime into standard React elements via [support.js](file:///Users/devang/Downloads/workstudio-hrm-design/project/support.js).
*   **Smooth Animations (GSAP)**: GSAP script tags power premium micro-animations, loading transitions, custom bar-graph loading flows, and counter number-rolling animations.
*   **Premium Typography & Layout**:
    *   Fonts: *Google Sans* & *Product Sans* for clean, modern interfaces.
    *   Styles: Fluid CSS layouts, glassmorphism aesthetics, radial gradient backgrounds, and responsive mobile-view structures.

---

## 📂 Project Structure

```bash
project/
├── WorkStudio.dc.html   # Main application markup containing structural HTML, CSS, and script data
├── support.js           # Runtime compiler parsing '<x-dc>' tags into a running React application
├── README.md            # Project overview and usage guidelines
└── .thumbnail           # Project thumbnail asset
```

---

## 🏃 Getting Started

Since WorkStudio is styled with vanilla CSS and loaded using client-side CDN scripts (React, GSAP), running it is simple:

### Option A: Local Browser
1.  Navigate to the project root directory.
2.  Open [WorkStudio.dc.html](file:///Users/devang/Downloads/workstudio-hrm-design/project/WorkStudio.dc.html) directly in any modern web browser (Double-click or drag-and-drop).

### Option B: Local Web Server (Recommended)
To prevent CORS policies from blocking certain async dynamic content or asset requests when loading:
```bash
# Using Node's serve utility
npx serve .

# Or Python's built-in server
python3 -m http.server 8000
```
Then, navigate to `http://localhost:3000` or `http://localhost:8000` in your browser.
