---
# Hephaestus Horizontal UI – Technical Specification

## 1. Overview
This document describes the horizontal layout UI for the Hephaestus SPA, inspired by the design in `context/Basic MSPaint UI.png`. The background image remains full-page, with a horizontally organized main content area.

## 2. Layout Structure
- **Background:**
  - Full-page background image (as in current implementation).
- **Main Content:**
  - Central horizontal flex container with the following sections (left to right):
    - **Sidebar Navigation:**
      - Vertical stack of icon buttons for Dashboard, Specialist, FUN, Chatbot/FAQ.
      - Collapsible on mobile (hamburger menu).
    - **Main Panel:**
      - Horizontally scrollable or wide flex area.
      - Contains horizontally arranged cards/sections for:
        - Dashboard (Checklist, Currency)
        - Specialist (Radar Chart, Metrics)
        - FUN Page (Rewards Grid)
        - Chatbot/FAQ (Tabbed Content)
      - Each section is a card with a semi-transparent or blurred background for readability.
    - **Optional Right Panel:**
      - Reserved for future About Me or notifications.
- **Footer:**
  - Minimal, fixed or sticky at the bottom.

## 3. Navigation & Responsiveness
- Sidebar navigation highlights the active section.
- On desktop, all main sections are visible side-by-side (or with horizontal scroll if needed).
- On mobile, sections stack vertically and sidebar collapses.
- Use Tailwind CSS flex and grid utilities for layout.

## 4. Styling
- Maintain full background image with overlay for content cards.
- Use Tailwind for spacing, rounded corners, and drop shadows.
- FontAwesome icons for navigation and UI elements.
- Animations for hover, active, and transitions.

## 5. Accessibility
- All navigation and controls are keyboard accessible.
- Sufficient color contrast and focus indicators.
- ARIA labels for navigation and tab controls.

## 6. Implementation Steps
1. Set up base HTML with Tailwind and FontAwesome CDNs.
2. Create a horizontal flex container for the main content area.
3. Build sidebar navigation as a vertical button group.
4. Create horizontally arranged content cards for each main section.
5. Style cards with semi-transparent backgrounds for readability.
6. Add responsive breakpoints for mobile stacking and sidebar collapse.
7. Add accessibility features (keyboard, ARIA).
8. Test layout on multiple devices and resolutions.

---
*This spec describes the horizontal UI layout for Hephaestus, matching the design intent of the provided reference image while keeping the immersive background.*
