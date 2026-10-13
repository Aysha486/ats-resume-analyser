# UI redesign notes

The UI has been refreshed without changing the resume-analysis algorithm or database model.

- Unified ATS ResumeAnalyser branding and navigation across pages
- Responsive desktop/mobile layout
- Updated upload form with a clearer PDF upload area and job-description field
- Dashboard metric cards and a cleaner recent-reports table
- Saved resumes displayed as cards with score badges
- Results page with score rings, matched/missing skill chips, and a resume-section checklist
- Updated login and registration pages
- Shared styles in `resumes/static/resumes/css/app.css`

The stylesheet uses Bootstrap 5 and Font Awesome from CDNs, so an internet connection is needed to load those external assets. The core layout remains usable without the icons and custom font.
