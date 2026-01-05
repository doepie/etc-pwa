# Eldoraigne Tennis Club - Business Requirements

## Project Overview
A web-facing PWA (Progressive Web App) designed to streamline the administration and operations of the Eldoraigne Tennis Club. The application avoids App Store certification by being "installable" directly from the browser.

## Phase 1: Committee Administration (Current Focus)
The initial release targets the Committee Members to handle daily club operations:
- **Duty Roster:** Manage shift duties with a "Swop-out" request system.
- **Financial Management:** Submit expense receipts or maintenance images via mobile camera directly to Google Drive (Root: etc-pwa/Finances), with metadata logged in Google Sheets.
- **Maintenance Log:** Report and track facility issues (plumbing, electrical, courts etc.).
- **Member Directory:** Sync membership status from booking JSON/Sheets to Google Contacts, applying specific labels and commentary.
- **Automated Communication:** LLM-assisted drafting for WhatsApp/Email reminders for birthdays and overdue payments.
- **Action Items:** Track committee meeting tasks and owners.
- **IoT Control:** Trigger club infrastructure (gates/lights) via cloud API calls.

## Phase 2: Club Members (Future)
Future expansion to allow general club members to:
- View their own duty dates.
- Access club documents (Google Drive view-thru).
- Receive push notifications for club news.

## Strategic Constraints
- **Zero-to-Low Cost:** Utilize Free Tiers of modern serverless infrastructure (Vercel, Supabase, Gemini).
- **Google Ecosystem:** Deep integration with Google Workspace (Sheets, Drive, People API).
- **Security:** Use Managed Auth and Row Level Security (RLS) to ensure committee data is protected.