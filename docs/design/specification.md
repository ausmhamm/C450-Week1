# Specification: School IT Support Knowledge Hub

App description: A simple web application for school staff to browse common technology problems and view troubleshooting steps before contacting IT staff.

## Style and Theme

The app should have a clean and professional look that is easy for school staff to use.

Overall mood: Simple, helpful, organized, and professional.

Use the **style-guide.html** for details on styling -- fonts, colors, and layout.

## User Scenarios

### Story 1 (most important)

A staff member is having a common technology problem and wants to solve it without contacting IT. They open the app, browse the support topics, select the issue they are having, and see troubleshooting steps for that problem.

---

## Requirements

### Functional Requirements

**R1.** The app must include these pages:
- Home (`#/`)
- Support Topics (`#/items`)
- Support Topic Detail (`#/items/:id`)
- About (`#/about`)

**R2.** The navigation bar must let people move to Home, Support Topics, and About.

**R3.** The app must load support topic data from `items-template.csv`.

**R4.** The Support Topics page must show one card for each support topic in the data file.

**R5.** Each card must include the topic name, short description, category, and image if available.

**R6.** Each card must include a way to open that topic's detail page.

**R7.** The detail page must show the full troubleshooting information for the selected support topic.

**R8.** Users should be able to bookmark or favorite support topics for easier access later.

**R9.** If the support data cannot load, the app must show a clear error message instead of a blank page.

### Key Data

- Support Topic
  - id
  - name
  - description
  - category
  - image_url
  - location

The `location` field may be reused or renamed later if another field is more useful for troubleshooting content.

## Success Criteria

1. A new user can open the app and reach the Support Topics page in one click from Home.
2. A new user can open one support topic detail page from the Support Topics page without help.
3. A user can understand the troubleshooting information shown on the detail page.
4. A user can bookmark or favorite a support topic.
5. If the data cannot load, the app shows a clear message instead of a blank page.

### Starter defaults

The template starts with Bootstrap default styling. The app should keep the Bootstrap-based layout while using a clean school/technology support style.

## Assumptions

- This is a prototype and not a finished production system.
- The app focuses on common school technology problems.
- The first version uses one text table data file as its data source.
- Placeholder images may be used when needed.
- Styling remains based on Bootstrap classes already used in the starter project.
- The first version focuses on browsing, viewing troubleshooting information, and simple bookmarking.
