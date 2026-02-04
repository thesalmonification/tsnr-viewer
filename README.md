🧠 Texas Society of Neuroradiology – Offline Abstract Viewer
A fully offline, browser-based abstract viewer designed for medical conferences and meetings.
This project allows attendees to browse scientific abstracts (PDFs) with search and filtering — no software installation and no internet connection required.
The system is intended to be distributed via USB flash drive and opened locally in any modern web browser.
✨ Features
📄 View abstracts as PDFs
🔍 Search by title, author, or institution
🗂 Filter by abstract category
📱 Mobile-friendly with collapsible menu
🖥 Optimized for conference kiosks and desktop displays
⚡ Works entirely offline
🔐 No admin privileges or installations required
📁 Folder Structure
abstract-viewer/
│
├── index.html          # Main application (open this file)
├── abstracts.js        # Abstract metadata (titles, authors, categories)
├── tsnr_logo.png       # Optional logo image
│
└── pdfs/
    ├── abstract_01.pdf
    ├── abstract_02.pdf
    ├── ...
    ├── abstract_20.pdf
    └── default.pdf     # Fallback PDF if an abstract is missing
🚀 How to Run (Offline)
Option 1: From USB Flash Drive (Recommended)
Copy the entire abstract-viewer folder onto a USB drive
Insert the USB drive into the target computer
Open the folder
Double-click index.html
The abstract viewer opens in your default web browser
Option 2: Copy to Local Computer
Copy the folder from USB to the desktop
Open index.html in a browser
✅ No internet connection required
✅ No local server needed
✅ No installation required
The application runs using the browser’s local file system (file://) and behaves like a local web app.
🌐 Browser Compatibility
Tested and supported in:
Google Chrome
Microsoft Edge
Firefox
Safari (desktop & mobile)
💡 Tip for kiosks: Press F11 (Windows) or ⌘ + Ctrl + F (Mac) for fullscreen mode.
🧩 Adding or Editing Abstracts
1️⃣ Add PDF Files
Place all abstract PDFs inside the pdfs/ folder.
Use consistent filenames, for example:
abstract_01.pdf
abstract_02.pdf
...
2️⃣ Update abstracts.js
Each abstract is defined as an object:
{
  title: "Abstract Title",
  category: "Scientific",
  author: "Jane Doe, MD",
  institution: "University of Texas",
  file: "abstract_01.pdf"
}
Supported categories are free-text (e.g. Scientific, Educational, Excerpta).
📄 Missing PDF Handling
If a listed PDF is not found, the viewer automatically loads:
pdfs/default.pdf
This prevents broken links and blank screens during the conference.
📱 Mobile & Tablet Use
On mobile devices, the abstract list collapses into a ☰ menu
Tap the menu button to browse abstracts
Selecting an abstract automatically closes the menu for reading
The layout automatically adapts based on screen size.
🔐 Security & Privacy
No network requests
No data collection
No tracking
All content stays on the local machine
Safe for use on hospital, academic, and conference computers.
🛠 Customization
Common customizations include:
Updating colors or branding
Adding institution logos
Adjusting categories
Changing layout spacing for large screens
All customization can be done by editing index.html and abstracts.js.
📦 Intended Use Case
Medical conferences
Academic meetings
Poster halls
Kiosk displays
USB-distributed content
Environments without internet access
📜 License
This project is intended for educational and conference use.
Add a license file if redistribution or reuse is planned.
🙌 Credits
Built for the Texas Society of Neuroradiology
Designed for reliability in restricted, offline environments.
