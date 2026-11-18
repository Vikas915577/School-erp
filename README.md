# ZenX School ERP — GitHub Pages Demo v0.4

A free, standalone, mobile-responsive frontend prototype for reviewing the ZenX School ERP experience. It contains five sample portals: Super Admin, School Admin, Teacher, Student, and Parent.

**This is a demo, not a production ERP.** The records are fictional. The payment, receipt, subscriptions, and notifications shown here are simulations; no money is collected and no real messages are sent.

## Publish it on GitHub Pages

The ZIP is deliberately arranged with `index.html` at the top level. GitHub Pages needs that file at the published folder's root.

1. Download and extract this ZIP on your computer or Android phone.
2. Open your GitHub repository in a browser.
3. Choose **Add file → Upload files**.
4. Upload the files *inside the extracted folder* (`index.html`, `.nojekyll`, `README.md`, `TEST-REPORT.md`, and `sample-students.csv`). Do not upload only the ZIP file; GitHub Pages will not extract it.
5. Commit the files to the repository's `main` branch.
6. Open **Settings → Pages**.
7. Under **Build and deployment**, select **Deploy from a branch**.
8. Choose branch **main** and folder **/(root)**, then press **Save**.
9. Open the Pages URL shown there. It usually looks like `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

No build command, Node.js, npm package, framework installation, backend, API key, or paid hosting is needed for this prototype. `.nojekyll` tells GitHub Pages to publish the static folder as-is.

### Android upload tip

In the Files app, extract the ZIP first. When selecting files for GitHub's upload page, select the files inside the extracted folder—not the parent folder and not the ZIP archive. Check that `index.html` appears in the repository's top-level file list after committing.

## Open and test the demo

- Use the portal selector in the top-right to switch between all five roles. There is no login screen in this demo.
- Use the left menu (or the menu icon on mobile) to open modules.
- School Admin → **Students** → **Add student** to test admissions.
- School Admin → **Attendance** to change and save attendance.
- School Admin or Parent → **Fees** to simulate a payment and update a sample balance.
- Teacher → **Homework** to create an assignment. Switch to Student or Parent to mark it submitted.
- Teacher → **Marks** to enter sample marks and publish a result.
- Super Admin → **Schools / Subscriptions / Support** to test tenant and support workflows.
- School Admin → **Students** → **Import CSV** to test importing. Use the included `sample-students.csv` file.
- Use the circular-arrow icon in the header to reset all demo changes to the original sample data. The browser asks for confirmation first.

Changes are intended to be stored in the current browser's `localStorage`. They are local to the browser and website origin: they are not shared with another user's browser or another device. Clearing site data or using the reset button clears the changes.

## Included files

- `index.html` — complete standalone demo application (HTML, CSS, and JavaScript in one file).
- `.nojekyll` — static publishing marker for GitHub Pages.
- `README.md` — this deployment and usage guide.
- `TEST-REPORT.md` — automated test summary and remaining limitations.
- `sample-students.csv` — sample import file with one valid student row.

## Demo coverage

- Role-specific navigation and dashboards for five roles.
- Student registration, profile editing, admission-number duplicate check, CSV import/export.
- Daily attendance register and read-only parent/student attendance view.
- Simulated fee collection, updated balance, payment history, and printable sample receipt.
- Homework creation and student/parent submission status.
- Exam scheduling, marks entry, grade calculation, and sample result publishing.
- School tenant creation/status, plan changes, sample support tickets.
- Staff, class section, notices, leave requests, reports, and school branding preview.
- Responsive layout for mobile, tablet, and desktop widths.

## Important limits before production

This frontend prototype does not include a real server, PostgreSQL database, secure login, true role authorization, API-side tenant isolation, production audit logs, cloud file uploads, backups, real UPI/payment collection, payment webhooks, SMS, WhatsApp, email delivery, push notifications, GPS, biometric hardware, or a compiled Android app. The role selector is only a demo navigation switch, not a security boundary. Transport and Library are sample/read-only views. Do not enter real student, parent, staff, or payment data into the public demo.

Production development must add a secure backend, database, authentication, server-side authorization and tenant isolation, privacy/security controls, verified payment-provider integrations, backup/restore, and deployment monitoring.

## Project contact details supplied

ZenX School ERP  
Mobile: 7060443998 / 9760443995  
Email: Ipandatprashant@gmail.com
