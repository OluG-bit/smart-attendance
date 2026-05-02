# OAU Smart Attendance System

A smart, GPS + WiFi verified attendance system for **Obafemi Awolowo University, Ile-Ife**.

## Features
- 🛡️ Three user roles: Admin, Lecturer, Student
- 📍 GPS proximity verification (≤150m from lecturer)
- 📡 WiFi network verification (same IP as lecturer)
- 📱 Device fingerprinting — one account per device
- 📄 Attendance sheet download (PDF & CSV)
- 🔒 Admin credentials are private and never shown in UI

## Login Credentials (Default)

| Role | Email | Password |
|------|-------|----------|
| Admin | adminoau@oauife.edu.ng | adminoau |
| Lecturer | Register with @oauife.edu.ng email | — |
| Student | Register with @student.oauife.edu.ng email | — |

## How Attendance Works
1. Lecturer opens a session for a course — system captures their **IP address** and **GPS location**
2. Student taps "Submit Attendance" — system checks:
   - ✅ Student's IP matches lecturer's IP (same WiFi)
   - ✅ Student is within **150 metres** of lecturer (GPS)
3. Both must pass — otherwise attendance is **rejected**

## Tech
- Pure HTML, CSS, JavaScript — no build step needed
- Hosted on Netlify (static)
- Data lives in-memory for the session

## Deployment
This site is deployed via [Netlify](https://netlify.com) directly from this GitHub repo.
Any push to `main` automatically redeploys.
