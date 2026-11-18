# ZenX School ERP — QA Test Report v0.5

Build: Premium GitHub Pages Demo v0.5  
Test date: 18 November 2026  
Browser engine: Chromium (headless Playwright automation)

## Summary

**All recorded test runs passed.** The suites overlap in some areas, so their counts should not be added as a unique-test total.

| Test suite | Result |
|---|---:|
| Premium UI, role portals, responsive layout, and main interactions | 65 / 65 passed |
| Core workflow regression suite | 26 / 26 passed |
| CSV import, printable receipt, and reset checks | 3 / 3 passed |
| Role/module rendering and role-access behavior | 50 / 50 passed |

## Premium UI and responsive checks — 65/65

- Standalone HTML loads and the redesigned overview banner/KPI cards render.
- All five portals render and expose their expected navigation destinations.
- Every listed module page renders without the generic unimplemented-page screen.
- Student admission and attendance-save interactions work.
- Parent fee collection opens the simulated payment form.
- No document-level horizontal overflow at 360px, 390px, 768px, and 1365px viewport widths.
- Mobile menu button measures 41×41 CSS pixels; navigation opens, routes, and closes after selection.
- No uncaught JavaScript errors or browser console errors in the tested session.

## Core workflow regression — 26/26

- Student admission creates a record; duplicate admission IDs are rejected.
- Attendance saves the updated student status.
- Simulated fee payment reduces the outstanding balance and adds a transaction-history entry.
- Teacher can create homework; Student can mark it submitted.
- Teacher can enter marks; marks and grade/result state update.
- Super Admin can add a school, change a plan, and create a support ticket.
- School branding settings save to the demo data state.
- Student CSV export downloads with the expected filename.
- Mobile navigation opens and routes to the selected module.
- No uncaught page errors or console errors in the tested session.

## Additional checks — 3/3

- CSV import accepted a valid sample row and skipped an invalid-mobile row.
- Printable fee receipt opened and clearly identifies itself as a demo receipt, not proof of payment.
- Reset restored the original six-student sample data.

## Role and module matrix — 50/50

- Expected navigation and rendering checked for every listed module across Super Admin, School Admin, Teacher, Student, and Parent.
- Teacher attendance editing remains limited to assigned sample classes.
- Parent and Student attendance screens are read-only.
- Parent dashboard supports child selection.
- Mobile navigation closes after choosing a module.

## Test method and limits

The exact `index.html` was loaded into Chromium and exercised with automated clicks, role switches, form entries, downloads, and responsive viewport changes. The isolated test document used an in-memory storage adapter because the test runner blocks local-file/localhost navigation and native `localStorage` access for its opaque document origin. This verified that application state changes and storage serialization calls are wired, but **native browser `localStorage` persistence after a refresh on the eventual GitHub Pages URL has not been independently verified**. After publishing, open the live Pages URL, create a test record, refresh, and confirm that it remains.

The test run did not publish to or access the user's GitHub repository. Actual GitHub Pages deployment still needs to be completed by uploading the extracted files. No real payment gateway, SMS/WhatsApp provider, email service, GPS or biometric device was connected. No backend, server-side security, production tenant isolation, or formal accessibility certification was tested.

## Release recommendation

Suitable for GitHub Pages UI review and a sample workflow demonstration with fictional records. Not suitable for live school operations or real personal/student data.
