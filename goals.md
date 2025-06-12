
## 🎯 Goal Journal

This document is for active journalling of personal and professional goals, using a structured format to enable clarity, reflection, and accountability.

---

### 🗓️ Daily Goals

#### 2025-06-13

**New Goals:**
  - ⭐ Implement MVP approach with nearly static site (pulling only projects from Sanity)
  - Simplify hero section to use static images and text
  - Simplify MobileNav to use static content
  - Begin building Projects module with Sanity integration
  - Clean up complex code that is no longer needed
  
**Focus Shift:**
  - Pivoting from full CMS-driven approach to a simpler MVP with limited Sanity integration
  - Prioritizing completion over advanced features like adaptive colors and accessibility automation

**Reflection:**
  - Yesterday's planning revealed that the complexity of the current architecture is slowing progress
  - A simplified approach will allow for faster delivery while maintaining core functionality

🕒 Time-Based Schedule:

| Time          | Task                                                            |
| ------------- | --------------------------------------------------------------- |
| 08:00 – 12:00 | Simplify Hero and MobileNav to use static images and text       |
| 12:00 – 13:00 | Lunch break                                                     |
| 13:00 – 16:00 | Start building Projects module with Sanity integration          |
| 16:00 – 17:00 | Clean up complex/unused code from previous approach             |



---

### 📅 Weekly Goals


### 📅 Weekly Goals

#### Week of 2025-06-10 (Updated)
**Top 3 Goals:**
- ✅ Define short-term and medium-term goals for Q2–Q3
- ✅ Map current project (web app) milestones to weekly objectives
- ⏳ Review secret startup documents
- 🔄 **Revised:** Create simplified MVP of Vanta web app with static content and Sanity integration only for Projects
- 🔄 **Revised:** Release MVP by end of June to allow client content management

**Notes / Reflections:**
Strategic shift to MVP approach will allow for faster delivery while meeting core client needs.

- **Completed:**

- **Notes / Reflections:**
  Set up an effective goal tracking system which will help monitor progress on these weekly goals.

#### Week of 2025-06-17

- **Goals:**
  1. Build first half of Vanta components

#### Week of 2025-06-24

- **Goals:**
  1. Build second half of Vanta components and finalize site

---

### 🗓️ Monthly Goals

#### June 2025

- **Focus Areas:**

  - Goal setting infrastructure
  - Vanta web app development

- **Objectives:**

  1. Complete the Vanta web app by June 30
  2. Develop a goal journaling habit (3+ entries/week)

- **Progress Review:**
  ✓ Made significant progress on goal journaling infrastructure (2025-06-11)

---

### 📆 Yearly Goals

#### 2025

- **Vision Statement:**

  - [To be defined]

- **Pillars of Focus:**

  - [To be defined]

- **Key Milestones:**

  - [To be defined]

- **Year-End Reflections:**

---

### 🧭 Context: Current Projects

#### Vanta Web App

- A custom marketing website for a local construction business.
- Built with Next.js, Tailwind CSS, Sanity CMS, deployed on Vercel.
- Desktop and mobile UI mockups complete.
- Core pages: Home, Projects, Project Detail, About, Reviews, Contact.
- Current development tasks:
  - Releasing a simplified version where clients can edit text and images on their website, except ones that affect accessibility.
  - Once released, based on user needs, consider finishing development of auto-accessible text over images.
- Delivery window for v1 June 2025.

#### Goal Tracking Initiative

- A structured journaling system to set and track personal and professional goals.
- Daily goals are written with ChatGPT and archived to [goals.kevd.design](https://goals.kevd.design).
- Each day's entry becomes a version-controlled snapshot, ensuring clarity and traceability.
- Enables mobile, voice-based journaling and goal-setting during daily routines like walking the dog.
- Acts as both a reference for ChatGPT and a durable accountability mechanism.

#### Secret Startup

- (Secret for now)

---

### 💡 Future Projects

#### Interactive Business Card Generator

- Users fill out a form to generate a stylized digital business card
- Data saved to a headless CMS
- Card displayed on your domain
- Optional contact option for custom domain mapping
- Inspired by JAMstack architecture

---

### 🕘 Past Days

#### 2025-06-12

**New Goals:**
  - Create simplify plan to refactor the code
  - Find a clean way to prevent unaccessible image edits in Sanity, while accessible image features are under development
  - Find a clean way to build the simplified app without losing progress made on the accessible image feature. (New webapp branch?)

**Failed Goals**
  - Complete MobileNav implementation (continued from June 11) - [Not completed by noon - see Fail Log](#-fail-to-succeed-log)

**Postponed Goals**
  - Update desktop Nav with matching features
  - Ensure the hero section has a rounded bottom edge as shown in the mockup
  - Begin work on "Project" component if time permits

**Reflection**
  - I've tried for the last few days to implement the MobileNav based on the Accessible Image features. Unfortunately it's too complex to transition and it's limiting my ability to finish at least a basic webapp by end of June.

🕒 Time-Based Schedule (Revised):

| Time          | Task                                                              |
| ------------- | ----------------------------------------------------------------- |
| 08:00 – 12:00 | Continue and complete MobileNav implementation ❌ (see [Fail Log](#-fail-to-succeed-log)) |
| 12:00 – 13:00 | Lunch break                                                       |
| 13:00 – 17:00 | 🛠️ Plan the pivot to simplifying the webapp. |

#### 2025-06-11

- **Goal(s):**

  - Finish goal setting by 11 a.m. (Extended – spent day configuring goal setting system)
  - Implement MobileNav with newest colorMap and Adaptive Color features (Started 4:00 p.m. – in progress)
  - Update desktop Nav with the same features (Moved to 2025-06-12)
  - Ensure the hero section has a rounded bottom edge (Moved to 2025-06-12)

- **Completed:**

  - Set up goals tracking system with GitHub Pages
  - Configured Jekyll for static Markdown rendering
  - Established DNS and proper website infrastructure

- **Notes / Reflections:**
  Spent more time than anticipated setting up the goal tracking infrastructure. This should pay dividends in the long run by providing a stable, version-controlled, and accessible system.

- 🕒 Revised Time-Based Schedule:

| Time          | Task                                                                      |
| ------------- | ------------------------------------------------------------------------- |
| 08:00 – 16:00 | Set up goal tracking system (GitHub Pages + Jekyll)                       |
| 16:00 – 18:00 | Implement MobileNav with colorMap + Adaptive Color features (in progress) |

---

## 📘 Fail to Succeed Log

### 🗓️ June 12, 2025

#### ❌ Missed Goal

**Implement MobileNav using accessibility feature**

#### 🔍 What I Tried

- Investigated why only the first 3 nav buttons were receiving adaptive backgrounds.
- Compared MobileNav with the working Hero component to uncover architectural differences.
- Identified a performance bottleneck: image accessibility recalculations on every resize and page load.
- Explored why the debug panel showed `text-white` while rendered text appeared black — traced it to multi-stage logic in AdaptiveText.
- Considered server-side processing for image accessibility using Sanity.

#### 🎓 What I Learned

- The adaptive image processing system is too brittle for MVP — leads to visual flicker and unnecessary re-rendering.
- Debugging dynamic styles is harder with layered decision-making in component logic.
- Server-side processing could reduce client overhead, but adds complexity too early.

#### 🔄 Pivot Strategy

- **Short-Term:** Phase out dynamic image accessibility for now. Use pre-selected images with hardcoded settings.
- **Launch Plan:** Restrict user-uploaded images in early release.
- **Long-Term:** Reintroduce advanced features post-launch with server-side analysis.
- **Core Change:** Shift focus to completing essential app functionality with simplified structure.

#### 🧭 Reframed Goal

**Finish webapp by June 30 with simplified, stable architecture.**
