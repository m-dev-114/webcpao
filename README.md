# Chief Pay & Accounts Office – A&N Administration Portal

A fully functional government web portal for the Chief Pay & Accounts Office, Andaman & Nicobar Administration.

---

## 🚀 Quick Start (VS Code)

### Option 1 – Open Directly (No server needed)
1. Open `index.html` in VS Code
2. Right-click → **Open with Live Server** (install the *Live Server* extension if needed)
3. Or simply double-click `index.html` to open in your browser

### Option 2 – Local HTTP Server (Python)
```bash
cd cpao_portal
python3 -m http.server 8080
# Open http://localhost:8080
```

### Option 3 – Node.js (npx serve)
```bash
npx serve cpao_portal
```

---

## 🌐 Deployment

### Deploy to Render (Free Static Site)
1. Push this folder to a GitHub repository
2. Go to [render.com](https://render.com) → New → **Static Site**
3. Connect your GitHub repo
4. Set:
   - **Build Command:** *(leave blank)*
   - **Publish Directory:** `.` (or `cpao_portal/`)
5. Click **Deploy** – your site will be live at `https://your-name.onrender.com`

### Deploy to Netlify (Drag & Drop)
1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag the entire `cpao_portal/` folder onto the page
3. Live instantly at a `*.netlify.app` URL

### Deploy to GitHub Pages
```bash
git init
git add .
git commit -m "Initial CPAO portal"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/cpao-portal.git
git push -u origin main
# Enable Pages in repo Settings → Pages → Deploy from main
```

---

## 🔑 Login Credentials (Demo)

| Role | User ID | Password |
|------|---------|----------|
| **Admin** | `admin001` | `admin123` |
| **Govt. Servant** | `AN-1042` | `servant123` |
| **Govt. Servant** | `AN-2078` | `pass2078` |

---

## ✅ Features

### Public (No Login Required)
- Home page with notices, ticker, quick links
- Staff Directory (view-only)
- Document & Forms library with **download** buttons
- Circulars & Office Orders with **download** buttons
- Contact page with officer list

### Admin Login (`admin001`)
- All public features +
- **Upload documents** with category tagging (publish to public list)
- **Add/Edit employee** records (staff directory management)
- **Add/Edit/Delete loan entries** – full loan register management
- View complete loan register with export button

### Govt. Servant Login (`AN-1042` or `AN-2078`)
- View their own **loan/advance status** with:
  - Visual progress tracker (step-by-step status)
  - EMI repayment progress bar
  - Balance outstanding
- Personal data tab in Loans & Advances section

---

## 📁 File Structure

```
cpao_portal/
├── index.html          # Single-file application (all HTML, CSS, JS)
└── README.md           # This file
```

All data is currently in-memory JavaScript arrays inside `index.html`.  
For production, replace with a backend API (FastAPI, Django, or Node.js) + database (PostgreSQL).

---

## 🔧 Customisation

### Change demo data
Edit the JavaScript arrays near the top of the `<script>` block:
- `staffData` – employee records
- `loansData` – loan & advance records  
- `docsData` – uploaded documents
- `circularsData` – circulars list

### Add real authentication
Replace the `USERS` object and `doLogin()` function with API calls to your backend.

### Add real file upload/download
Replace `uploadDocument()` and `downloadDoc()` with fetch calls to your file storage endpoint (e.g., AWS S3, NIC Object Store).

---

## 📞 Support
Chief Pay & Accounts Office, A&N Administration  
Port Blair – 744 101 | Phone: 03192-232271
