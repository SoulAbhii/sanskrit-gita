📘 Bhagavad Gītā — Svelte Webpage

A fully responsive, pixel-perfect recreation of the Bhagavad Gītā page from Sanskrit.ie, built using Svelte + Vite, featuring:
✔ Accurate UI replication
✔ Clean responsive layout
✔ Custom navigation bar
✔ Scroll-to-top button
✔ Chapter grid (1–18)
✔ Footer with social icons
✔ Ready for API integration
✔ Deployed on Vercel

🌐 Live Demo

Vercel Deployment:
👉 (https://gita-sanskrit.netlify.app/)

📂 Project Structure
gita-svelte/
│
├── public/
│   ├── images/         # All static assets (hero image, book, icons, footer bg)
│   └── favicon.svg
│
├── src/
│   ├── components/     # Navbar, footer, chapters, hero section
│   ├── routes/         # (If using SvelteKit)
│   ├── App.svelte
│   └── main.js
│
├── package.json
├── vite.config.js
└── README.md


🚀 Features
1. Fully Recreated Bhagavad Gītā Hero Section

Background chariot image

Top white overlays (exact like Sanskrit.ie)

Title typography (edensor, Noto Sans Devanagari)

Overlapping open-book image

Mobile-responsive scaling

2. Custom Navigation Bar

Logo on the left

Search icon next

Navigation links on the right

Down-arrow icon added

Burger menu for mobile

Mobile-side panel navigation

3. Chapter Grid (1–18)

Diamond-shaped chapter icons

Background book image perfectly fitted

Number overlay with dark stripe

Fully responsive grid (7→6→4→3→2 columns)

Accessible link labels

4. Footer

Footer background image

Social icons

Centered logo

“WELLBEING-SVASTI” typography

Copyright row

Responsive arrangement

5. Scroll to Top Button

Fixed bottom-right button

Smooth scroll

White-bordered button

Arrow animation on hover

🛠️ Tech Stack
Frontend

Svelte — component framework

Vite — build tool

HTML5 / CSS3

Responsive design (media queries)

Tools & Deployment

Git / GitHub

Vercel — hosting + CI/CD

🧩 Installation

Clone the repository:

git clone https://github.com/SoulAbhii/sanskrit-gita.git
cd YOUR-REPO


Install dependencies:

npm install


Start the development server:

npm run dev


Open your browser:

http://localhost:5173

📦 Building for Production

Generate the optimized production build:

npm run build


Preview the build locally:

npm run preview


Build output goes to:

dist/


📜 License

This project is created for educational + assignment purposes.
All rights to original Sanskrit.ie design belong to their creators.

👨‍💻 Developer

Abhishek Sah
Frontend Developer (React / Svelte)
