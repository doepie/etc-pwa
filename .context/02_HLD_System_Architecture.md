# High-Level Design (HLD) & Tech Stack

## 1. Explicit Tech Stack
- **Framework:** Next.js 15+ (App Router, TypeScript).
- **Styling:** Tailwind CSS (Custom Design Tokens).
- **Database/Auth:** Supabase (PostgreSQL, Auth, RLS).
- **Storage:** Google Drive API (Root: `etc-pwa/`).
- **Communication:** Resend (Email), 3rd Party QR Provider (WhatsApp).
- **Intelligence:** Google Gemini 1.5 Flash/Pro (via Vercel AI SDK).
- **PWA:** Serwist (Service Workers/Manifest).

## 2. Centralized Notification Service (The "Post Office")
- **Purpose:** A single internal service that handles all outgoing messages.
- **Logic:**
    1. Check `notification_configs` for `USE_AI` toggle.
    2. If `AI=ON`: Send Prompt + Context (Member, Date, Event) to Gemini.
    3. If `AI=OFF`: Use Static Template with `{{handlebars}}` placeholders.
    4. Delivery: Route to Email, WhatsApp, or both based on config.

## 3. UI/UX Strategy
- **Master-Detail Layout:** Consistent with `ui_prototype.html`.
- **Responsive:** Sidebar (PC) / Drawer (Mobile).
- **Tokens:** Primary Blue `#0B3173`, Accent Gold `#D4AF37`.