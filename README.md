# StudyBuddy AI  

**An elegant, client‑side web app that uses Google Gemini to explain topics, generate quizzes, and build personalised study plans.**  

![StudyBuddy banner](screenshots/banner.png) <!-- optional banner image -->

---

## 📖 Table of Contents  

1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Live Demo (GitHub Pages)](#live-demo-github-pages)  
4. [Setup & Installation](#setup--installation)  
   - [1️⃣ Clone the repo](#1-clone-the-repo)  
   - [2️⃣ Obtain a Gemini API key](#2-obtain-a-gemini-api-key)  
   - [3️⃣ Run the app locally](#3-run-the-app-locally)  
5. [Usage Guide](#usage-guide)  
   - [Explain a Topic](#explain-a-topic)  
   - [Generate a Quiz](#generate-a-quiz)  
   - [Create a Study Plan](#create-a-study-plan)  
6. [Design & Architecture](#design--architecture)  
7. [Screenshots](#screenshots)  
8. [Known Limitations & Troubleshooting](#known-limitations--troubleshooting)  
9. [Future Work](#future-work)  
10. [Contributing](#contributing)  
11. [License](#license)  
12. [Acknowledgements](#acknowledgements)  

---

## 🎯 Project Overview  

StudyBuddy AI is a **single‑page HTML/JS application** that showcases how to integrate a large‑language model (Google Gemini) directly in the browser without any server‑side component.  

- **Zero‑install** – just open `index.html` in any modern browser.  
- **Dynamic model fallback** – the app tries four free‑tier Gemini models (`gemini‑2.0‑flash‑lite`, `gemini‑2.5‑flash‑lite`, `gemini‑2.0‑flash`, `gemini‑2.5‑flash`) in order, gracefully handling quota exhaustion.  
- **Local API‑key storage** – the key is saved in `localStorage` so you only paste it once per device.  
- **Responsive, premium UI** – glass‑morphism background, smooth micro‑animations, dark‑mode‑compatible palette, and a consistent design system built with vanilla CSS variables.

The repo is deliberately lightweight so it can be submitted as a Kaggle capstone **without any build tools**.

---

## ✨ Features  

| Feature | Description |
|--------|-------------|
| **Explain** | Provide a short‑summary + detailed explanation + a real‑world analogy + three fun facts for any user‑supplied topic. |
| **Quiz Generator** | Create a 5‑question multiple‑choice quiz (easy/medium/hard difficulty) with correct‑answer indices and brief explanations, all returned as JSON from Gemini and rendered instantly. |
| **Personalised Study Plan** | Build a day‑by‑day plan (5‑14 days) with 2‑4 actionable tasks per day, based on a free‑form user goal (e.g., “Learn Python in 7 days”). |
| **Model Fallback & Quota Handling** | Automatic retry on 429 responses; when all free‑tier quotas are exhausted the UI shows a friendly “wait a while” message and suggests enabling billing. |
| **API‑Key Validation** | Accepts both historic `AIza…` keys **and** the new 2026 `AQ.…` format, displaying clear error messages for malformed keys. |
| **Copy‑to‑Clipboard** | One‑click copy for explanations, quiz results, and study plans. |
| **Responsive Layout** | Works on desktop, tablet, and mobile screens; UI collapses gracefully on narrow viewports. |
| **Dark‑mode ready** | All colours are defined via CSS variables; the dark background is the default but can easily be tweaked. |

---

## 🚀 Live Demo (GitHub Pages)

The repository is configured to serve the app via **GitHub Pages**.  
If you enable Pages on the `main` branch (Settings → Pages → Source: `main` / `/ (root)`), the app will be reachable at:
