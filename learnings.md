# Learning & UI Patterns

## Key Realizations

### 1. The "Stretch" Layout Pattern
* **Problem:** Job cards were either too small (fitting short text) or overflowing (long text) when using `width: 100%`.
* **Solution:** Set the parent container to `display: flex` and `flex-direction: column`, then use **`align-items: stretch`**. This forces all children to match the width of the parent container perfectly regardless of the content inside.

### 2. Spacing Control
* **Lesson:** AI often mixes margins and paddings, leading to "shrunk" or overlapping elements. 
* **Fix:** Explicitly command the AI to use **`gap`** for layout spacing and **`padding`** for internal breathing room. Prohibit the use of `margin` for better predictability.

### 3. Visual Distinction for Tags
* **Design Pattern:** For relevant tags/pills, always specify a **border-radius** (e.g., `pill` or `rounded-full`) and a **border variable** (e.g., `border-100`) to ensure they don't blend into the card background.

---

## 🛠 Refined Technical Table

| Component | Issue Encountered | Prompt Fix / Instruction |
| :--- | :--- | :--- |
| **Containers** | Logic floating in header | "Group [X] and [Y] into a `nav-left` container." |
| **Job Cards** | Width inconsistency | "Remove Width 100% and use `align-items: stretch` on parent." |
| **AI Badges** | Low contrast/visibility | "Use white background with `border-100` and `text-muted`." |
| **Spacing** | Elements too close | "Apply consistent `gap-4` and avoid margins." |

---

## The "Golden" Component Checklist
*Use these specific phrases in future prompts to avoid common layout failures:*

- [ ] **"Use variables already defined in the CSS file"** (Prevents hardcoded hex codes).
- [ ] **"Ensure child elements stretch to fill the container width"** (Prevents narrow cards).
- [ ] **"Group related elements into logical sub-containers"** (e.g., nav-left, nav-right).
- [ ] **"Use a monochrome palette with soft borders (border-100)"** (Maintains brand consistency).

---

## 📅 Log History
* **2025-12-27:** Solved Flexbox stretching issues on Job List.
* **2025-12-27:** Refined Navbar structure with sub-containers for better alignment.