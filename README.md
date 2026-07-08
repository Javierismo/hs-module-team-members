# HubSpot Team Members Module

Reusable HubSpot CMS module that renders a team directory from HubDB with editor-controlled labels, field mapping, and card styling.

## Overview

This project provides a reusable HubSpot module for displaying team members from a HubDB table in a responsive card grid. It is designed to stay flexible across projects where HubDB column names and content structures may vary.

## Key Features

- HubDB-powered team directory rendering
- Configurable HubDB column mapping for easier reuse across tables
- Optional department-based filtering
- Responsive team card grid for desktop and mobile
- Editor-friendly labels and style controls
- Module-scoped color tokens injected with HubL

## Accessibility

- Semantic section and article markup
- Configurable `aria-label` for the contact links group
- Descriptive `aria-label` values for email and social links

## Technologies

- HubL
- HTML
- CSS

## Installation

1. Add the module folder to your HubSpot theme modules directory.
2. Upload the theme or module to your HubSpot account.
3. Open a page or template in Design Manager.
4. Insert the Team Members module into the layout.
5. Select the HubDB table and configure the field mappings in the page editor.

## Module Structure

- `modules/team-members.module/module.html` -> handles HubDB retrieval, filtering, and markup output.
- `modules/team-members.module/module.css` -> contains the team card styles and responsive grid.
- `modules/team-members.module/module.js` -> reserved for future enhancements. The current version does not require JavaScript.
- `modules/team-members.module/fields.json` -> defines editor controls for HubDB mapping, labels, and styles.
- `modules/team-members.module/meta.json` -> registers the module in HubSpot.

## Customization

Main configurable fields include:

- Section title and intro copy
- HubDB table selection
- Sort column and direction
- Department filter
- HubDB column mapping for name, role, department, bio, photo, and links
- Empty-state and accessibility labels
- Card background, border, and text colors

## Responsive Behavior

- Mobile: single-column card layout
- Tablet: two-column grid from `640px`
- Desktop: three-column grid from `960px`

## Why This Project

This module was built to prioritize maintainability and real production needs:

- Editors can manage team content from HubDB without touching code.
- Column mapping makes the module easier to reuse across accounts and projects.
- Styling is scoped to the module to reduce theme-wide side effects.
- The structure stays simple enough to extend later with richer profile actions or filters.

## Data Requirements

The module expects a HubDB table that includes columns for the values you map in the editor, typically:

- `name`
- `role`
- `department`
- `bio`
- `photo`
- `email`
- `linkedin_url`
- `x_url`

You can change these column names in the module fields to match your own HubDB schema.

## Preview

### Desktop view

![Team Members - Desktop](assets/team-members.jpg)

### Mobile view

![Team Members - Mobile](assets/menu-mobile.jpg)

## Author

Developed by **Javier Fuentes**

- GitHub: https://github.com/Javierismo
