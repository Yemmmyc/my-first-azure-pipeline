# 🌌 Nebula UI App

![Azure Static Web Apps](https://img.shields.io/badge/Deployment-Azure%20Static%20Web%20Apps-blue) ![React](https://img.shields.io/badge/Framework-React-blueviolet) ![Node.js](https://img.shields.io/badge/Node.js-18.20.8-green)

> A modern, responsive static web app built with **React**, deployed on **Azure Static Web Apps**, featuring clean architecture and easy CI/CD integration.

---

## 🎯 Project Aim
The **Nebula UI App** is designed to demonstrate:
- A full React front-end app with optimized production build.
- Continuous Deployment using **Azure Static Web Apps**.
- Proper GitHub Actions workflow setup for automated CI/CD.
- Best practices in project structure, `.gitignore`, and secret management.

---

## 🗂 Project Structure
```text
nebula-ui-app/
├── nebula-ui/              # React app source code
│   ├── public/
│   ├── src/
│   └── package.json
├── .github/
│   └── workflows/
│       └── azure-static-web-apps.yml  # CI/CD workflow
├── .gitignore
└── README.md
```

---

## ⚡ Features
- Responsive React UI
- Fast production build
- CI/CD with GitHub Actions → Azure
- Environment-safe secrets via GitHub Secrets
- Clear separation of source and build directories

---

## 🚀 Deployment Steps

### 1️⃣ Connect Repo to Azure
1. Create a **Static Web App** in the Azure Portal.
2. Link **GitHub repository**.
3. Do **not let Azure generate workflow** if one exists.

### 2️⃣ Set GitHub Secrets
- Add `AZURE_STATIC_WEB_APPS_API_TOKEN` (from Azure) to GitHub secrets.

### 3️⃣ Workflow Configuration
```yaml
app_location: "nebula-ui"
api_location: ""
output_location: "nebula-ui/build"
```

### 4️⃣ Build & Deploy
- `npm install` → install dependencies
- `npm run build` → generate optimized production build
- GitHub Actions workflow triggers deployment automatically

---

## ⚙️ Technologies Used
| Technology | Version / Type |
|------------|----------------|
| React      | 18.x           |
| Node.js    | 18.20.8        |
| GitHub Actions | CI/CD        |
| Azure      | Static Web Apps |

---

## 🛠 Local Setup
1. Clone the repository:
```bash
git clone https://github.com/Yemmmyc/my-first-azure-pipeline.git
cd my-first-azure-pipeline/nebula-ui
```
2. Install dependencies:
```bash
npm install
```
3. Run the development server:
```bash
npm start
```
4. Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## ✅ Deployment Workflow
![CI/CD Workflow](https://github.com/Yemmmyc/my-first-azure-pipeline/actions/workflows/azure-static-web-apps.yml/badge.svg)

1. Push to `main` branch.
2. GitHub Actions builds React app.
3. Oryx prepares the production build.
4. Azure Static Web Apps hosts the app automatically.

---

## 🔧 Troubleshooting
- **BadRequest / API Key invalid** → verify token in GitHub Secrets.
- **Artifact folder missing** → check `output_location` in workflow.
- **Node version mismatch** → ensure Node version in workflow matches local project.

---

## 📸 Screenshots & GIFs
![App Screenshot](https://via.placeholder.com/600x400.png?text=Nebula+UI+App+Screenshot)
![Deployment GIF](https://media.giphy.com/media/3oEjI6SIIHBdRxXI40/giphy.gif)

---

## 📌 Notes
- Only one active workflow is recommended.
- Always keep `.gitignore` updated to avoid unnecessary commits.
- Monitor GitHub Actions logs for deployment issues.

---

## 📝 Author
**Yemisi** – IT & DevOps Enthusiast  