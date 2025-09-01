### Changes and Configuration Notes

- Social icons
  - Using existing Font Awesome (CDN) to keep dependencies minimal and consistent with the stack.
  - Icons are added via the `buttonLink` helper in `index.html`, which prepends icons, adds `aria-label`, and preserves focus states.
  - Footer now renders GitHub and LinkedIn links with icons using the same helper.

- Sidebar order
  - Defined once in `index.html` via `NAV_ITEMS` under the "Tabs & Navigation" section.
  - The sidebar is generated from `NAV_ITEMS`, and `TABS` is derived from it to avoid duplication.
  - Order (top → bottom): Summary, Work Experience, Publications, Education, Projects, Skills.

- Skills progress bars
  - Proficiency levels are provided in `RESUME_YAML` (`skills.items[].level`, scale 0–5).
  - `progressBar` renders accessible progress bars (`role="progressbar"`, `aria-valuenow`, and `aria-label`).
  - Bars animate width on initial render for smooth visual feedback.

- Mobile sidebar toggle button
  - Increased mobile header stacking order to ensure the hamburger button is visible (`z-50`).
  - Button declares `aria-controls="sidebar"` and `aria-expanded` for accessibility.

No heavy dependencies were introduced; all updates are within the existing single-file, CDN-based architecture.


