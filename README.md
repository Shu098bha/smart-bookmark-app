# 🚀 Smart Bookmark App

A full-stack bookmark manager built using Next.js (App Router), Supabase, Google OAuth, and Tailwind CSS.

---

##  Features

- Google Login (OAuth authentication only)
- Add bookmarks (Title + URL)
- Each user sees only their own bookmarks
- Real-time updates using Supabase Realtime
- Delete bookmarks
- Deployed on Vercel (Production Ready)

---

##  Tech Stack

- Next.js 16 (App Router)
- Supabase (Auth + Database + Realtime)
- Google OAuth
- Tailwind CSS
- Git & GitHub
- Vercel (Deployment)

---

##  Live Demo

https://smart-bookmark-app-gold-kappa.vercel.app

---

##  Installation (Local Setup)

Run the following commands:

npm install
npm run dev

Then open:

http://localhost:3000

---

##  Problems I Faced & How I Solved Them

### 1 PowerShell Execution Policy Error

Problem:
npx cannot be loaded because running scripts is disabled

Solution:
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned

---

### 2 Row Level Security Blocking Data

Problem:
Bookmarks were not visible after inserting.

Cause:
Row Level Security (RLS) was enabled but policies were not defined.

Solution:
Created RLS policy using:

auth.uid() = user_id

This ensured users can only view and modify their own bookmarks.

---

### 3 Supabase Environment Variables Not Working on Vercel

Problem:
Deployment failed with error: supabaseUrl is required

Cause:
Environment variables were not added in Vercel.

Solution:
Added the following in Vercel project settings:

NEXT_PUBLIC_SUPABASE_URL  
NEXT_PUBLIC_SUPABASE_ANON_KEY  

Then redeployed the project.

---

### 4 Port 3000 Already in Use

Problem:
Next.js dev server could not start because port 3000 was busy.

Solution:
Stopped existing Node process and restarted with:

npm run dev



### 5 Git Authentication Error

Problem:
Git required username and email before committing.

Solution:

git config --global user.name "Shubha Naik"  
git config --global user.email "your-email@example.com"

---

## 💡 Future Improvements

- Edit bookmark feature
- Search bookmarks
- Add categories
- UI animations
- Dark / Light mode toggle

---

## 👩‍💻 Author

Shubha Naik
