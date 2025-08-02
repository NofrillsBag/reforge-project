# Hephaestus App Product Requirements Document (PRD)

## Overview
Hephaestus is a gamified rehabilitation web app designed to increase user agency and engagement for patients who may be overwhelmed or unsure where to start. The app uses checklists, metrics, and rewards to motivate users and adapt to their needs, prioritizing actionable feedback over passive chatbot interactions.

## Core Pages & Features

### 1. Dashboard View
- **Purpose:** Central hub for daily checklists, currency counter, and overall status.
- **Features:**
  - Taskbar with daily checklists
  - Currency counter (earned by completing tasks)
  - Visual feedback on progress

### 2. Chatbot View
- **Purpose:** Facet-specific bots and FAQ for user support.
- **Features:**
  - Tabbed interface for mental, physical, social, and cognitive support
  - FAQ section

### 3. The FUN Page
- **Purpose:** Reward system where users spend currency to unlock Pexels backgrounds.
- **Features:**
  - Grid of locked/unlocked backgrounds
  - Currency-based unlocking
  - Persistent background selection

### 4. Patient About Me
- **Purpose:** Collect personal data, preferences, and self-reported metrics.
- **Features:**
  - Form inputs for PHQ, GAD, Likert, sentiment
  - Sliders, dropdowns, and emoji inputs
  - Save data to localStorage (simulate MongoDB)

### 5. Specialist View
- **Purpose:** Visualize patient metrics for specialist review.
- **Features:**
  - Chart.js radar chart of 4 pillars (Emotional, Physical, Social, Cognitive)
  - Patient summary

## App Philosophy
- Gamification to drive engagement
- Closed-loop rehab: Measure → Adapt → Motivate
- Focus on actionable, adaptive planning
- Prioritize users who are overwhelmed or unsure what to ask

## Stack & Tools
- **Styling:** Tailwind CSS (CDN)
- **Icons:** FontAwesome Jelly Pack
- **Charts:** Chart.js (Radar + Line)
- **Media/Rewards:** Pexels backgrounds
- **Logic:** Vanilla JS
- **Storage:** localStorage (MongoDB later)

## User Stories & Acceptance Criteria

### Dashboard Checklist & Currency
- **User Story:** As a user, I want to check off daily tasks and earn currency so I feel rewarded for my progress.
- **Acceptance Criteria:**
  - [ ] Checking a task adds +1 currency
  - [ ] Currency total is visible and updates live
  - [ ] Checklist and currency persist via localStorage

### About Me Data Collection
- **User Story:** As a user, I want to enter my mood and preferences so the app can personalize my experience.
- **Acceptance Criteria:**
  - [ ] Form includes PHQ, GAD, Likert, and sentiment inputs
  - [ ] Data is saved to localStorage
  - [ ] Data can be updated and persists across sessions

### Specialist Radar Chart
- **User Story:** As a specialist, I want to see a radar chart of patient metrics so I can quickly assess their status.
- **Acceptance Criteria:**
  - [ ] Radar chart displays Emotional, Physical, Social, Cognitive scores
  - [ ] Data is pulled from localStorage
  - [ ] Chart updates when new data is entered

### FUN Page Rewards
- **User Story:** As a user, I want to spend my earned currency to unlock backgrounds so I feel motivated to complete tasks.
- **Acceptance Criteria:**
  - [ ] Locked backgrounds are shown in a grid
  - [ ] Unlocking a background deducts currency
  - [ ] Unlocked backgrounds persist across sessions

### Chatbot & FAQ
- **User Story:** As a user, I want to access facet-specific chatbots and FAQs so I can get help tailored to my needs.
- **Acceptance Criteria:**
  - [ ] Tabbed interface for each support area
  - [ ] FAQ is searchable (Fuse.js, stretch goal)

## Team Roles
- **UI Lead:** Tailwind layout, icons, nav/footers
- **Logic Lead:** Checklist logic, PHQ/GAD storage, currency
- **Chart Lead:** Radar/Line charts, score imports
- **Content Lead:** Chatbot text, FAQ, user guidance

## Stretch Goals
- Daily reset for checklists
- Persistent background selection
- Form export as PDF
- Fuse.js FAQ search
- Gemini-based journaling/emotion summarizer

---

*This PRD is a living document. Update as features are refined or new requirements emerge.*
