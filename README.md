# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build

A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)

Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

✅ This proof must be visible in your browser screenshot submission.

---

## Footer Version and Deploy Date

The portfolio footer shows the version, deployment date, and author:

```html
<p>Pravin Mishra Portfolio v1.0 — Deployed on <span id="deployDate"></span> — By Kuntal Tarwatkar</p>
```

The deployment date is generated automatically using JavaScript in `DD Mon YYYY` format.

Example:

```javascript
const deployDate = new Date();

const months = ["Jan", "Feb", "Mar", "Apr", "May", "Jun",
                "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"];

const formattedDate =
  String(deployDate.getDate()).padStart(2, "0") +
  " " +
  months[deployDate.getMonth()] +
  " " +
  deployDate.getFullYear();

document.getElementById("deployDate").textContent = formattedDate;
```

This avoids manually changing the date each time the portfolio is deployed.
