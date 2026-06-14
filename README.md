# 🏢 Shubh Nisarg CHS Ltd — Society Hub Portal

Society Management Portal for Shubh Nisarg CHS Ltd, Badlapur, Thane, Maharashtra.

**Live URL:** https://shubhnisarg.github.io/societyhub

---

## ✅ Modules Included

| Module | Description |
|---|---|
| ⚙️ Setup | One-time Google Sheets header writer |
| 👥 Members | Master list of flat owners |
| 🏦 Cheque Payments | Record cheques from members with image capture |
| 💵 Cash Withdrawal | Track petty cash given to committee members |
| 📊 Expense Tracker | Log all expenses (utility, salaries, etc.) with invoice capture |
| ⚖️ Cash Tracker | Petty cash reconciliation + liability calculator |
| 📁 View Records | Browse, search, filter and export all data |

---

## 🔧 One-Time Configuration

Before deploying, open `src/App.jsx` and fill in the **CONFIG** block at the top (around line 21):

```js
const CONFIG = {
  SPREADSHEET_ID: "paste-your-spreadsheet-id-here",
  CLIENT_ID:      "paste-your-oauth-client-id-here",
  SCOPES:         "https://www.googleapis.com/auth/spreadsheets https://www.googleapis.com/auth/drive.file",
  DRIVE_FOLDER_ID:"paste-your-drive-folder-id-here",
};
```

### How to get each value:

**SPREADSHEET_ID**
- Open your Google Sheet
- Copy the long ID from the URL:
  `https://docs.google.com/spreadsheets/d/THIS_PART/edit`

**CLIENT_ID**
- Go to https://console.cloud.google.com
- Create a project → Enable Google Sheets API + Google Drive API
- APIs & Services → Credentials → Create OAuth 2.0 Client ID → Web Application
- Add Authorised JavaScript Origins: `https://shubhnisarg.github.io`
- Add Authorised Redirect URIs: `https://shubhnisarg.github.io/societyhub`
- Copy the Client ID

**DRIVE_FOLDER_ID**
- Create a folder in Google Drive called "Shubh Nisarg CHS Images"
- Open it and copy the ID from its URL

---

## 🚀 Deployment — Step by Step

### Step 1: Install Git (if not already)
Download from https://git-scm.com/downloads and install.

### Step 2: Install Node.js (if not already)
Download from https://nodejs.org (choose LTS version) and install.

### Step 3: Download this project
Download the ZIP of all these files and extract to a folder on your computer,
OR clone using:
```bash
git clone https://github.com/shubhnisarg/societyhub.git
cd societyhub
```

### Step 4: Fill in your CONFIG values
Open `src/App.jsx` in any text editor (Notepad, VS Code, etc.)
Find the CONFIG block and paste your values.

### Step 5: Enable GitHub Pages in your repo
- Go to https://github.com/shubhnisarg/societyhub
- Settings → Pages → Source → **GitHub Actions**
- Save

### Step 6: Push your code to GitHub

If you cloned the repo (Step 3 option 2):
```bash
git add .
git commit -m "Initial portal setup with config"
git push origin main
```

If you downloaded the ZIP, open terminal/command prompt in the extracted folder:
```bash
git init
git add .
git commit -m "Initial portal setup"
git branch -M main
git remote add origin https://github.com/shubhnisarg/societyhub.git
git push -u origin main
```

### Step 7: Wait for deployment
- Go to https://github.com/shubhnisarg/societyhub/actions
- You'll see a workflow running called "Deploy to GitHub Pages"
- Wait 2–3 minutes for it to complete (green tick ✅)

### Step 8: Open your portal
Visit: **https://shubhnisarg.github.io/societyhub**

---

## 🔄 Updating the Portal Later

Whenever you make changes to any file:
```bash
git add .
git commit -m "describe what you changed"
git push origin main
```
GitHub Actions will automatically rebuild and redeploy within 2–3 minutes.

---

## 📞 Support
Portal built for: Shubh Nisarg CHS Ltd, Badlapur, Thane, Maharashtra
