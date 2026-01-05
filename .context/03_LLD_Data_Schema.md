# Low-Level Design (LLD): Data Schema

## 1. Supabase Tables
### Table: `profiles`
- `id` (UUID), `uid` (ETC-XXXX), `email`, `preferred_name`, `role` (Admin|Treasurer|Committee), `is_committee` (Bool).

### Table: `notification_configs`
- `key` (PK), `use_ai` (Bool), `selected_model` (Text), `prompt_template` (Text), `static_template` (Text), `trigger_days` (Int).

### Table: `maintenance_logs` / `action_items`
- Fields as per prototype (Status, Owner_UID, Description, Date).

## 2. Google Sheets
- **Members_Master:** `UID, FirstName, LastName, PreferredName, Email, Phone, Birthday, IsCommittee`.
- **Roster_2026:** `Date (YYYY/MM/DD), Day, EventName, MemberUID, DisplayName`.