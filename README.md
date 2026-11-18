# ZenX School ERP — Premium GitHub Pages Demo v0.5

A free, standalone, responsive frontend prototype for reviewing the ZenX School ERP experience. It includes five role-based demo portals: Super Admin, School Admin, Teacher, Student, and Parent.

**This is a frontend demo, not a production ERP.** All records are fictional. Fees/payments, receipts, subscription actions, support requests, and school data changes are simulations stored in the current browser only. No money is collected and no real messages are sent.

## What changed in v0.5

- Premium, consistent UI system: midnight-navy navigation, soft neutral workspace, cobalt and teal accents, clearer spacing, refined cards, readable tables, and polished forms.
- Role-specific overview banner copy for Super Admin, School Admin, Teacher, Student, and Parent.
- More usable mobile layout with a collapsible navigation drawer, larger touch controls, compact KPI cards, and stacked dashboard panels.
- Improved hover/focus states, clearer status chips, more legible helper text, and reduced-motion support.
- Existing demo actions and sample workflows have been retained.
- No external fonts, CSS frameworks, JavaScript libraries, build tools, paid APIs, or server are required.

## Publish on GitHub Pages

The ZIP has `index.html` at its root. GitHub Pages needs that file in the published folder's root.

1. Download this ZIP and extract it on your Android phone or computer.
2. Open your GitHub repository.
3. Select **Add file → Upload files**.
4. Upload the files inside the extracted folder: `index.html`, `.nojekyll`, `README.md`, `TEST-REPORT.md`, and `sample-students.csv`. Do not upload only the ZIP; GitHub does not extract it automatically.
5. Commit the files to the `main` branch.
6. Open **Settings → Pages**.
7. Under **Build and deployment**, select **Deploy from a branch**.
8. Choose branch **main** and folder **/(root)**, then select **Save**.
9. Open the GitHub Pages URL displayed in Settings. It usually looks like `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

No build command, Node.js, npm install, framework setup, API key, backend, or paid hosting is needed for this static prototype. `.nojekyll` tells GitHub Pages to publish the folder as-is.

### Android upload tip

In the Files app, extract the ZIP first. On GitHub's upload page, choose the files inside the extracted folder—not just the parent folder and not the ZIP archive. After committing, check that `index.html` is visible at the top level of the repository.

## Explore the demo

- Use the portal selector in the top-right to switch between all five roles. There is no actual login system in this demo.
- Use the left navigation on desktop or the menu button on mobile to open modules.
- **School Admin → Students → Add student** to create a sample admission. Duplicate admission IDs are rejected.
- **School Admin → Attendance** to change and save sample attendance.
- **School Admin → Fees** or **Parent → Fees** to simulate a payment and update a sample fee balance.
- **Teacher → Homework** to create an assignment. Switch to Student or Parent to mark it submitted.
- **Teacher → Marks** to enter sample marks and view grade calculations.
- **Super Admin → Schools / Subscriptions / Support** to try tenant, plan, and support workflows.
- **School Admin → Students → Import CSV** to test importing. Use the included `sample-students.csv` file.
- Use the refresh/reset icon in the header to restore the original sample data. The browser asks for confirmation.

Changes use the current website origin's `localStorage`. This means the data is local to that browser and website address; it is not shared with other users or devices. Clearing website data or resetting the demo removes those changes.

## Files in this ZIP

- `index.html` — complete standalone demo (HTML, CSS, and JavaScript in one file).
- `.nojekyll` — GitHub Pages publishing marker.
- `README.md` — this guide.
- `TEST-REPORT.md` — test coverage, results, and remaining limitations.
- `sample-students.csv` — sample student import file with one valid row.

## Demonstration coverage

- Role-specific navigation and overview dashboards for all five portals.
- Student admission, profile edits, duplicate-ID validation, CSV import/export.
- Daily attendance register and read-only Student/Parent attendance views.
- Simulated fee collection, updated balances, payment history, printable sample receipts.
- Homework creation and Student/Parent submission status.
- Exam scheduling, marks entry, grade calculation, and sample result publishing.
- School tenant creation/status, subscription plan changes, sample support tickets.
- Staff, class sections, notices, leave requests, reports, transport/library sample views, and branding preview.
- Desktop, tablet, and mobile-responsive navigation and layouts.

## Important limits before production

This prototype does **not** include a real server, PostgreSQL database, secure login, production role authorization, server-side tenant isolation, live audit logs, cloud file uploads, backups, actual UPI/payment collection, payment webhooks, SMS, WhatsApp, email delivery, push notifications, GPS, biometric hardware, or a compiled Android app. The role selector is only a demonstration control—not a security boundary. Transport and Library are sample/read-only views. Do not enter real student, parent, staff, or payment data into a public demo.

Production development must add a secure backend, database, authentication, server-side permissions and tenant isolation, privacy/security controls, verified payment-provider integrations, tested backup/restore, monitoring, and the Android application.

## Contact details supplied for ZenX School ERP

- Mobile: 7060443998 / 9760443995
- Email: Ipandatprashant@gmail.com

## UI/UX references used

The mobile navigation and touch-friendly sizing were informed by the official Android responsive-navigation guidance and WCAG 2.2. The refreshed skin uses dark readable text, visible focus states, larger touch controls, and responsive navigation. This is a design-informed prototype, not a formal accessibility certification.

- [W3C — Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
- [Android Developers — Responsive UI and navigation](https://developer.android.com/guide/navigation/responsive/config-changes)
