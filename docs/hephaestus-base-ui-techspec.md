---
# Hephaestus Base UI – Technical Specification

## 1. Overview
This document describes the base UI structure and layout for the Hephaestus Single Page Application (SPA). The design prioritizes clarity, accessibility, and a gamified, engaging user experience. All navigation and content updates occur without full page reloads.

## 2. UI Structure

### 2.1. Main Layout
- **Header/Navbar:**
  - Fixed at the top.
  - Contains navigation buttons/icons for: Dashboard, About Me, Specialist, FUN Page, Chatbot/FAQ.
  - Responsive: collapses to a hamburger menu on mobile.
  - Uses Tailwind CSS for styling and FontAwesome for icons.

- **Main Content Area:**
  - Contains all page views as separate div containers (one per view).
  - Only one view is visible at a time; others are hidden via CSS.
  - Views:
    - Dashboard (checklist, currency)
    - About Me (form)
    - Specialist (radar chart)
    - FUN Page (rewards grid)
    - Chatbot/FAQ (tabbed interface)

- **Footer:**
  - Fixed or sticky at the bottom.
  - Contains copyright, quick links, or motivational messages.

### 2.2. Navigation Logic
- Navigation buttons update the visible view by toggling CSS classes (e.g., `hidden`, `block`).
- No page reloads; all state and UI updates are handled in JavaScript.
- Active navigation item is visually highlighted.

## 3. Page View Details

### 3.1. Dashboard View
- Checklist of daily tasks (checkboxes + labels)
- Currency counter (prominently displayed)
- Visual feedback for completed tasks (e.g., color change, animation)

### 3.2. About Me View
- Form with sliders, dropdowns, and text area for PHQ, GAD, Likert, sentiment
- Save/Update button
- Pre-populate fields from localStorage

### 3.3. Specialist View
- Chart.js radar chart visualizing four pillar metrics
- Patient summary section

### 3.4. FUN Page
- Grid of backgrounds (locked/unlocked)
- Unlock/select buttons
- Currency cost displayed on locked items

### 3.5. Chatbot/FAQ View
- Tabbed interface for Mental, Physical, Social, Cognitive, FAQ
- Each tab shows static content or FAQ list

## 4. Styling & Responsiveness
- Use Tailwind CSS utility classes for layout, spacing, and responsiveness
- FontAwesome icons for navigation and UI elements
- Mobile-first design: all views adapt to small screens
- Animations for feedback (e.g., hover, task completion)

## 5. Accessibility
- All navigation and controls are keyboard accessible
- Sufficient color contrast and focus indicators
- ARIA labels for navigation and tab controls

## 6. Implementation Steps
1. Set up base HTML with Tailwind and FontAwesome CDNs
2. Create header/navbar, main content area, and footer
3. Build each view as a separate div container
4. Implement navigation logic in JavaScript to show/hide views
5. Style all components for desktop and mobile
6. Add accessibility features (keyboard, ARIA)
7. Test navigation and layout on multiple devices

---
*This spec describes the foundational UI for the Hephaestus SPA. All further features and logic will build on this structure.*
