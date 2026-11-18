# ZenX School ERP — QA Test Report

Build: GitHub Pages Demo v0.4  
Test date: 18 November 2026  
Browser engine: Chromium 144 (headless automation)

## Result

**79 automated checks passed; 0 failed.**

### Core workflow and browser checks — 26/26 passed

- Standalone HTML loaded and main dashboard rendered.
- School Admin role selection and portal rendering.
- Add student, persist the new student to the browser storage API, and reject duplicate admission ID.
- Save attendance and verify changed attendance in the saved demo state.
- Simulated fee payment reduces outstanding balance and adds a payment-history record.
- Teacher creates homework; Student submits it.
- Teacher enters marks; marks and published result state update correctly.
- Super Admin creates a school tenant and updates its subscription plan.
- Super Admin creates a support ticket.
- School branding name and colour settings save.
- CSV export downloads with the expected filename.
- Mobile menu opens and routes to the selected module.
- No uncaught page errors and no browser console errors during tested flows.
- No document-level horizontal overflow at 360px, 390px, 768px, or 1365px viewport widths.

### Role and module checks — 50/50 passed

- All five role selectors and role-specific navigation lists matched expected modules.
- All role module pages rendered without the generic unimplemented-page message.
- Teacher attendance editing was limited to the sample assigned classes.
- Parent and Student attendance pages were read-only.
- Parent dashboard displayed child switching.
- Mobile menu opened and closed after choosing a navigation item.

### Additional workflow checks — 3/3 passed

- CSV import added the valid sample row and skipped a row with an invalid mobile number.
- A printable sample fee receipt opened and clearly stated that it is not proof of a real payment.
- Reset restored the original six-student sample dataset.

## Test method and limits

The exact standalone `index.html` was loaded in Chromium and driven through its UI with automated clicks, form entries, role switches, and downloads. A small in-memory storage adapter was used by the test harness because the isolated test document has an opaque browser origin and the environment blocks localhost navigation. This verified the app's save/serialization calls, but **native `localStorage` persistence after a refresh on the eventual GitHub Pages URL has not been independently verified**. The browser test also did not publish to or access the user's GitHub repository. After uploading, verify the actual GitHub Pages URL and refresh persistence in your own browser.

The test environment did not connect any real payment gateway, SMS/WhatsApp provider, email service, GPS or biometric device. No backend or server-side security was tested because those services are not part of this frontend demo.

## Release recommendation

Suitable for GitHub Pages UI review and workflow demonstration using fictional sample records. Not suitable for live school operations or real personal/student data.
