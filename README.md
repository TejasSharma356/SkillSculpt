# 📄 SkillSculpt

A full-stack **Resume Builder** built with the **React (TailwindCSS)** frontend and **Firebase backend** for authentication and storage.  
Users can log in, create multiple resumes with names, edit them dynamically, preview live updates, and export them as PDFs.  

---

## 🚀 Features
- 🔐 **User Authentication** with Firebase (Login / Signup).  
- 🏠 **Dashboard** where users can:
  - View all their resumes (stored in Firebase).  
  - Create new resumes with a custom name.  
  - Select and edit existing resumes.  
- 📝 **Resume Form** with fields for:
  - Resume Name (so users can manage multiple resumes)  
  - Personal details  
  - Education  
  - Experience  
  - Projects  
  - Skills  
- 👀 **Live Resume Preview** that updates instantly as you type.  
- 📥 **Export as PDF** with one click.  
- 💾 **Save and Edit later** → resumes are stored in Firebase Firestore under each user’s account.  

---

## 🏗️ Tech Stack

### **Frontend**
- ⚛️ React (Vite)  
- 🎨 TailwindCSS for styling  
- 🧩 shadcn/ui + Lucide icons (UI components)  
- 📄 `jspdf` for PDF export  

### **Backend**
- 🔥 **Firebase Authentication** (email/password login)  
- 🔥 **Firebase Firestore** (to store user resumes in collections per user)  
- 🔥 **Firebase Hosting** (optional for deployment)  

---

## 📂 Project Structure
```
resume-builder/
│── src/
│   ├── components/
│   │   ├── Login.jsx
│   │   ├── Dashboard.jsx
│   │   ├── ResumeForm.jsx
│   │   ├── ResumePreview.jsx
│   ├── App.jsx
│   ├── firebase.js  # Firebase config & setup
│── public/
│── package.json
│── README.md
```

---

## 🔧 Installation & Setup
1. Clone the repo:
   ```
   git clone https://github.com/yourusername/resume-builder.git
   cd resume-builder
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Setup Firebase:
   - Go to Firebase Console: https://console.firebase.google.com/  
   - Create a new project.  
   - Enable **Authentication (Email/Password)**.  
   - Enable **Firestore Database**.  
   - Get your Firebase config keys and add them in `src/firebase.js`:  

   ```js
   // src/firebase.js
   import { initializeApp } from "firebase/app";
   import { getAuth } from "firebase/auth";
   import { getFirestore } from "firebase/firestore";

   const firebaseConfig = {
     apiKey: "YOUR_API_KEY",
     authDomain: "YOUR_AUTH_DOMAIN",
     projectId: "YOUR_PROJECT_ID",
     storageBucket: "YOUR_STORAGE_BUCKET",
     messagingSenderId: "YOUR_MSG_SENDER_ID",
     appId: "YOUR_APP_ID"
   };

   const app = initializeApp(firebaseConfig);
   export const auth = getAuth(app);
   export const db = getFirestore(app);
   ```

4. Run the app:
   ```
   npm run dev
   ```

---

## 📝 Roadmap (Completed ✅)

- ✅ **Login & Authentication** (Firebase Email/Password)  
- ✅ **Dashboard** with list of resumes per user  
- ✅ **Create New Resume** with a custom name  
- ✅ **Resume Form** (Personal, Education, Experience, Projects, Skills)  
- ✅ **Resume Preview** (updates live as you type)  
- ✅ **Export Resume as PDF**  
- ✅ **Save Resumes in Firestore** (per user)  
- ✅ **Edit Existing Resumes** (load data from Firestore and update)  
- ✅ **Delete a Resume** from Dashboard  

---

## 📌 Deployment
- Deploy frontend with **Vercel / Firebase Hosting**  
- Backend is **Firebase (serverless)**, so no extra server setup needed.  

---

## 👨‍💻 Author
Built by Tejas Sharma ✨  
