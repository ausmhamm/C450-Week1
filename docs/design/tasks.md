# Tasks — School IT Support Knowledge Hub

> Derived from the plan document. Each task is small, checkable, and traceable to a requirement.

## Task List

| ID | Task | Traces to (R# / ADR#) | Depends on | Status |
|---|---|---|---|---|
| T1 | Inspect the starter application routes, CSV loading, and current page structure | ADR-00 | — | Not started |
| T2 | Adapt the starter CSV records into a small set of school IT support topics | R3, ADR-01 | T1 | Not started |
| T3 | Update navigation labels and page text for Home, Support Topics, and About | R1, R2, ADR-03 | T1 | Not started |
| T4 | Adapt the Support Topics view to render one card per CSV row | R3, R4, ADR-01 | T2 | Not started |
| T5 | Update each card to show name, short description, category, and image when available | R5 | T4 | Not started |
| T6 | Add or verify the control that opens the selected topic detail page | R6, ADR-03 | T4 | Not started |
| T7 | Adapt the detail view to show full troubleshooting information | R7, ADR-03 | T6 | Not started |
| T8 | Test collection-to-detail navigation with multiple support topics | R4, R6, R7 | T5, T7 | Not started |
| T9 | Add simple bookmark/favorite controls | R8, ADR-04 | T5, T7 | Not started |
| T10 | Store and restore bookmarked topic IDs using browser storage | R8, ADR-04 | T9 | Not started |
| T11 | Add a visible error message for CSV/data-load failure | R9, ADR-05 | T4 | Not started |
| T12 | Test the data-load failure state | R9, ADR-05 | T11 | Not started |
| T13 | Apply the clean school IT support theme while keeping Bootstrap structure | R1, R2, R4-R7, ADR-02 | T3, T5, T7 | Not started |
| T14 | Check the main pages and cards on narrow and wide browser sizes | R1, R2, R4-R7, ADR-02 | T13 | Not started |
| T15 | Test the full Story 1 flow from Home to Support Topics to one detail page | R1-R7 | T8, T13 | Not started |
| T16 | Test bookmarking by saving a topic, refreshing, and confirming it remains saved | R8, ADR-04 | T10 | Not started |
| T17 | Review the finished prototype against all requirements and success criteria | R1-R9 | T12, T14, T15, T16 | Not started |

**Status values:** Not started · In progress · Done · Blocked

## Definition of Done (applies to every task)
- Matches its linked requirement's acceptance criteria in the specification.
- Reviewed by a human before marked done
- No task marked done without a test passing

## Blocked / Questions

| Task | Blocker | Raised | Resolved |
|---|---|---|---|
| | | | |
