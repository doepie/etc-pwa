# Business Requirement Specification (BRS)

## 1. Executive Summary
A PWA for Eldoraigne Tennis Club to manage committee operations. Generic and evolvable.

## 2. Core Functional Modules (Menu-Driven)
- **Operations > Club Roster:**
    - Interactive Calendar (PC) & List (Mobile).
    - Logic: Sync from Google Sheet 'Roster_2026'.
    - Action: "Request Swop" triggers the Centralized Notification Service.
- **Finance > Claims & Receipts:**
    - Action: Snap receipt -> Client-side compress -> Upload to G-Drive `etc-pwa/Finances` -> Log to G-Sheet.
    - Dashboard: Treasurer-only view to cycle status (Pending|Review|Paid).
- **Administration > Member Sync:**
    - Sync external Booking JSON to Google Contacts.
    - Apply Labels: "Club Member 2026" and update Notes with status/commentary.
- **Administration > Actions:**
    - Task tracker for committee meetings (Due Date, Owner, Status).

## 3. Centralized Notification Requirements
- **Automated Reminders:** Duty reminders at 7, 3, and 1 day(s).
- **Weekly Summary:** Every Monday at 07:00, a WhatsApp summary of the week's roster to the committee group.
- **Birthdays:** Daily check at 08:00; send greeting via WhatsApp/Email.
- **User Control:** Admin must be able to toggle AI (Gemini) ON/OFF and select the AI model.