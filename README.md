# **🚌 Smart Bus Stop Request System**

🔗 [Live Demo](https://bus-request-app-87702.web.app/)

A lightweight, cost-free internal tool for smart transport planning — designed during my internship at Tata Elxsi to solve a real challenge employees face when using company buses with inconsistent stop schedules.

🧩 Problem
Company buses follow fixed routes, but not all buses stop at every point. One day, I had to walk back from a junction because the driver didn’t see me stand up at my stop. This led to a question:

💡 What if there was a system that could show drivers exactly where to stop each day based on passenger requests?

✅ Features
     Separate logins for passengers and drivers (via Firebase Auth)
     Passengers select a stop via map UI
     Temporary stop creation when no fixed stop is nearby (within 60m)
     Drivers see only today's requested stops, shown on map
     Fixed routes (A, B, C) with polylines plotted on Leaflet.js
     Company email verification using Firebase + optional Google Sheets
     Data stored in Firestore – live and synced in real-time
     Minimal clean UI in shades of blue
    100% Free-tier deployment (no paid APIs)

🏗️ Tech Stack
Tool	Purpose
    Firebase Auth	Secure login, access control
    Firestore	Realtime DB for users/stops
    Leaflet.js	Interactive maps & routing
    Google Sheets	Admin approval system (opt)
    HTML/CSS/JS	Lightweight frontend

📦 Firebase Structure

plaintext
Copy
Edit
routes/
  A/
    stops/         ← name, lat, lng, order, temp: true?
  B/
stop_requests/
  { email, route, stop, createdAt }
users/
  { email, role }  ← optional for role-based access
  
🔐 Company Email Verification

To restrict access, only company emails (e.g., @tataelxsi.com) are allowed. You can extend this using Google Sheets + Apps Script for:

  Approval-based onboarding
  Email domain whitelisting
  Logging and admin controls

Roadmap

   Mobile-responsive layout
   Route optimization / clustering logic
   Driver/passenger analytics dashboard
   Admin dashboard with manual override
   Notification system (email/SMS alerts)

📸 Screenshots
<img width="1919" height="1019" alt="Screenshot 2025-07-13 033039" src="https://github.com/user-attachments/assets/d2c935f1-ffed-448b-9fb7-eb29c3aee270" />
<img width="1911" height="963" alt="Screenshot 2025-07-13 040741" src="https://github.com/user-attachments/assets/be6bc14c-2709-435c-a2cf-c1170400dac6" />
<img width="1902" height="959" alt="Screenshot 2025-07-13 040814" src="https://github.com/user-attachments/assets/ecb011ba-eb32-4fa0-9c05-15f0d5819008" />
<img width="1898" height="962" alt="Screenshot 2025-07-13 040835" src="https://github.com/user-attachments/assets/489e8b97-14de-40a4-ac52-4acd6d27c627" />




💬 Acknowledgements
  This system was independently conceptualized and developed as a practical solution to a recurring issue during my internship. While it was inspired by my time at Tata Elxsi, all design and development were initiated by me, and the platform runs entirely on free-tier services.

  ## License

This project is licensed under the [MIT License](LICENSE).

