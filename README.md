# 🧠 Texas Society of Neuroradiology – Abstract Viewer

A browser-based abstract viewer for the Texas Society of Neuroradiology annual meeting.
Attendees can browse, search, and read scientific abstracts (PDFs) from any device.

🔗 **Live site:** [https://tsnr-viewer.vercel.app](https://tsnr-viewer.vercel.app)

---

## ✨ Features

- 📄 View abstracts as PDFs directly in the browser
- 🔍 Search by **title**, **author**, or **institution**
- 🗂 Filter by abstract category (Scientific, Educational, Excerpta, Posters)
- 🖥 Desktop: PDFs open embedded in the viewer pane
- 📱 Mobile: PDFs open in a new tab for full-screen reading
- 📲 QR code on desktop for easy handoff to a phone
- 🌐 Hosted on Vercel — no installation required

---

## 📁 Folder Structure

```
tsnr-viewer/
│
├── index.html          # Main application
├── abstracts.js        # Abstract metadata (titles, authors, categories, filenames)
├── tsnr_logo.png       # Logo image
├── favicon.ico         # Browser tab icon
│
└── pdfs/
    ├── Scientific/
    ├── Educational/
    ├── Excerpta/
    └── Posters/
```

PDFs are organized into subfolders matching their abstract category.

---

## 🧩 Adding or Editing Abstracts

### 1️⃣ Add PDF Files

Place each PDF in the appropriate category subfolder under `pdfs/`:

```
pdfs/Scientific/My Abstract Title.pdf
pdfs/Posters/Another Abstract.pdf
```

### 2️⃣ Update `abstracts.js`

Each abstract is an entry in the `abstracts` array:

```js
{
  title: "Abstract Title",
  category: "Scientific",       // Must match a subfolder name under pdfs/
  author: "Jane Doe, MD",
  institution: "University of Texas",
  file: "My Abstract Title.pdf"
}
```

The `file` field is the PDF filename only — the path is constructed automatically from the category.

---

## 🚀 Deployment

The site is deployed via [Vercel](https://vercel.com) from this GitHub repository.
Pushing to `main` triggers an automatic redeploy.

To run locally, simply open `index.html` in a browser — no server is required.

---

## 🌐 Browser Compatibility

Tested and supported in:

- Google Chrome
- Microsoft Edge
- Firefox
- Safari (desktop & mobile)

---

## 📱 Mobile Behavior

On screens narrower than 900px:

- The PDF viewer is hidden; the abstract list takes the full screen
- Tapping an abstract opens the PDF in a new browser tab
- The QR code widget is hidden (it's intended for desktop kiosk use)

---

## 🛠 Customization

All customization is done by editing `index.html` and `abstracts.js`:

- Colors and branding: CSS variables at the top of `index.html`
- Abstract data: `abstracts.js`
- Categories: free-text strings that must match subfolder names under `pdfs/`

---

## 🙌 Credits

Built for the **Texas Society of Neuroradiology**.
