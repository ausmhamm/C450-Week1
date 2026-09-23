# Plan — School IT Support Knowledge Hub

> Written after specification. Every decision here must trace back to a requirement ID.

## 1. Approach Summary

The School IT Support Knowledge Hub will be built by adapting the existing starter web application into a simple support-topic browser for school staff. The first version will use the provided CSV data source, Bootstrap-based layout, and existing route structure. Work will focus on a clear front-end prototype with support-topic cards, detail pages, simple bookmarking, and useful error messages.

## 1.5 Tech Stack

- Frontend: Existing HTML/JavaScript starter application with Bootstrap
- Backend/DB: None for the first prototype
- Hosting: GitHub Pages
- Other services/APIs: `items-template.csv`; browser storage for simple bookmarks if supported by the starter code

## 2. Key Decisions (ADRs)

| ADR # | Decision | Traces to (R#) | Alternatives considered | Why this one |
|---|---|---|---|---|
| ADR-00 | Adapt the existing starter application instead of rebuilding it | R1-R9 | Rebuild from scratch | Keeps the project focused on required behavior and avoids unnecessary rewrite work. |
| ADR-01 | Use `items-template.csv` as the prototype data source | R3-R7, R9 | Add a database now | The specification already requires the CSV file and this phase is a front-end prototype. |
| ADR-02 | Keep Bootstrap and make only project-specific visual changes | R1, R2, R4-R7 | Replace Bootstrap | The starter already uses Bootstrap, so keeping it reduces unnecessary work. |
| ADR-03 | Reuse the existing item routes but label them as Support Topics and Support Topic Detail | R1, R2, R4-R7 | Create a new routing system | The existing collection/detail pattern already matches the app requirements. |
| ADR-04 | Store simple bookmarks in browser storage for the prototype | R8 | Add accounts and database-backed favorites | Browser storage supports the requirement without adding backend work. |
| ADR-05 | Show a visible message when support-topic data cannot load | R9 | Leave the page blank or console-only | A visible error directly supports the success criteria. |

## 3. Components / Building Blocks

| Component | Purpose | Related requirements |
|---|---|---|
| Home page | Introduces the app and gives users a path to Support Topics | R1, R2 |
| Navigation bar | Lets users move between Home, Support Topics, and About | R2 |
| Support Topics view | Displays one card per support topic | R3, R4, R5 |
| Support Topic card | Shows summary information and opens the detail view | R5, R6 |
| Support Topic detail view | Shows full troubleshooting information for one topic | R6, R7 |
| Bookmark/favorite control | Lets users save useful topics | R8 |
| About page | Explains the purpose of the app | R1, R2 |
| CSV data file | Stores prototype support-topic data | R3-R7 |
| Error state | Shows a clear message if the data cannot load | R9 |

## 4. Dependencies & Assumptions

- External services/tools needed: GitHub repository, GitHub Pages, starter application, Bootstrap.
- Assumption: `items-template.csv` can be adapted to hold the needed support-topic information.
- Assumption: The starter already has basic routes for Home, collection, detail, and About.
- Assumption: Bookmarking can be handled with browser storage for the prototype.
- Assumption: The first version only needs a small set of representative support topics.
- Assumption: The `location` field may be renamed or repurposed later if needed.

## 5. Risks

| Risk | Likelihood | Impact | Mitigation | Owner |
|---|---|---|---|---|
| CSV fields do not fit support topic content well | Medium | Medium | Adapt only the minimum necessary fields and document any changes | Austin |
| Starter structure differs from plan assumptions | Medium | Medium | Inspect the starter code before implementation and adjust tasks instead of rewriting | Austin |
| Bookmarking becomes more complicated than needed | Low | Medium | Keep bookmarks local to the browser and avoid user accounts | Austin |
| Cards become cluttered with too much text | Medium | Low | Keep cards short and move full troubleshooting content to the detail page | Austin |
| Data-load failure leaves the page unusable | Low | Medium | Add and test a visible error state | Austin |
| Styling becomes inconsistent | Low | Low | Keep Bootstrap and limit custom styling to theme/readability changes | Austin |

## 6. Sequencing

1. Inspect the starter application and confirm routes, CSV loading, and current structure.
2. Adapt the starter data into school IT support topics.
3. Update navigation and page labels.
4. Build or adapt the Support Topics collection view.
5. Build or adapt the Support Topic detail view.
6. Add simple bookmark/favorite behavior.
7. Add the visible data-load error state.
8. Apply final school IT support styling.
9. Test the full user flow against the specification.

## 7. Review & Approval

| Reviewer | Date | Approved? |
|---|---|---|
| Austin Hammond | 9/22/26 | Yes |

**Gate:** Do not generate tasks until this plan is done.
