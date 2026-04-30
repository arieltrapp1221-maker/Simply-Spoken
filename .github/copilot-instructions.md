# Simply Spoken - AI Coding Guide

## Project Overview

**Simply Spoken** is a static poetry website designed as a digital space for creative expression through multiple poetry forms. The site features a curated collection of prompts, poetry type education, user submissions, and a personal poetry gallery.

### Architecture
- **Frontend-only**: Pure HTML/CSS/JavaScript (no backend services)
- **Multi-page site**: Six main pages connected via consistent navigation
- **Static forms**: Data collection forms present but not integrated with persistence layer
- **Aesthetic focus**: Georgia serif typography, warm earth-tone palette (#FAF7F2, #4E3B31, #A3B18A)

## Key Components & Patterns

### Navigation Structure
All pages use an identical navbar component with brown background (#4E3B31) and beige links (#E8DDCF). Located in each HTML file starting at `<nav class="navbar">`. When modifying navigation:
- Update the navbar in **every** HTML file (index.html, written.html, poetry.html, prompts.html, seen.html, forms.html)
- Keep link order consistent: Home → Written → Poetry Types → Prompts → Seen → Submit

### Styling & Design System
- **Font**: Georgia serif (poetry aesthetic)
- **Color palette**:
  - Background: #FAF7F2 (cream)
  - Text: #4E3B31 (dark brown)
  - Nav/Accent: #4E3B31
  - Hover state: #A3B18A (sage green)
- **CSS organization**: Global reset → Typography → Component sections (navbar, hero, etc.)
- Style changes should respect existing color scheme and serif typography throughout `style.css`

### Page Templates
Each page follows a consistent template with navbar, content section, and footer styling. The form page (forms.html) uses `.form-page` container and `.poetry-form` styling for consistent input appearance.

### JavaScript Implementation
Current JavaScript is minimal (`script.js`). The `showPrompt()` function demonstrates basic interactivity through alerts. When adding features:
- Keep functionality simple and client-side focused
- Use vanilla JavaScript (no external frameworks)
- Consider form submission handling for the poetry form

## File Organization

```
/images/          - Hero and page background images (home.jpg referenced)
forms.html        - Poem submission form with name, email, poetry type, text
index.html        - Home/landing page with hero section
poetry.html       - Educational content on poetry types/forms
prompts.html      - Grid-based writing prompts with cards
seen.html         - Gallery/display of existing poems
written.html      - About/essay section
style.css         - Unified styling for all pages
script.js         - Minimal interactive functions
```

## Development Conventions

1. **HTML structure**: Follow semantic HTML; navbar is repeated pattern across pages
2. **CSS styling**: Maintain Georgia serif font family in body; preserve warm earth-tone color scheme
3. **Responsive design**: Use flexbox for navbar and grid layouts (evident in prompt-grid, form layouts)
4. **Links**: All pages link back through navbar; use relative paths (e.g., `href="index.html"`)
5. **Forms**: Use placeholder attributes and `required` validation; submit handling not yet implemented

## When Adding Features

- **New pages**: Copy navbar from existing page; maintain consistent styling via style.css
- **New prompts/content**: Add to appropriate HTML file; update navbar if creating new navigation item
- **Style updates**: Modify style.css globally to maintain consistency across all pages
- **Interactivity**: Add to script.js; ensure vanilla JavaScript approach
- **Images**: Place in `/images/` directory; reference with relative paths

## Design Philosophy

Simply Spoken prioritizes aesthetic and emotional resonance over complexity. The design emphasizes contemplative typography (serif), warm colors, and a poetry-first focus. Keep code simple, readable, and supportive of this creative mission.
