# Product Requirements Document (PRD) - Todo App Upgrade: Due Dates, Priority, Filters

## 1. Overview

We are upgrading the basic Todo app (currently supporting `title` and `completed`) to add due dates, simple priorities, and filter views so users can quickly identify what is due today and what is overdue, without adding backend complexity. This MVP is intentionally lightweight and teachable, using local storage only.

---

## 2. MVP Scope

- Data Model:
  - `title`: required.
  - `priority`: enum "P1" | "P2" | "P3"; default "P3".
  - `dueDate`: optional ISO date string `YYYY-MM-DD`; invalid values are ignored (treated as absent).
- Filters:
  - Views: All, Today, Overdue.
  - Behavior: All shows completed tasks; Today and Overdue show only incomplete tasks.
- Storage:
  - Local storage only; no backend or external storage.
- General Constraints:
  - Keep UI simple; accessibility/keyboard navigation enhancements are not required in MVP.

---

## 3. Post-MVP Scope

- Visual Overdue Highlighting:
  - Overdue tasks visually indicated (e.g., red highlight) to stand out.
- Sorting Rules:
  - Order: Overdue first → Priority (P1→P3) → Due date ascending → Undated last.
- Priority Badges (Visual):
  - Color-coded badges for priority (e.g., P1 red, P2 orange, P3 gray).

---

## 4. Out of Scope

- Notifications.
- Recurring tasks.
- Multi-user features.
- Keyboard navigation/accessibility enhancements beyond basic usability.
- External storage or backend changes (stay local-only).
