# Specification: Finance & Claims

## 1. Google Drive Directory Structure
The application will maintain a strict hierarchy in Google Drive:
- **Root Folder:** `etc-pwa`
- **Finance Root:** `etc-pwa/Finances`
- **Monthly Folders:** `etc-pwa/Finances/2026/01_January`, `etc-pwa/Finances/2026/02_February`, etc.

## 2. Receipt Upload Workflow
1. **User Action:** Committee member opens the PWA "Submit Receipt" form.
2. **Compression (Client-Side):**
   - Use `browser-image-compression`.
   - Max Width: 1280px.
   - Max Size: 500KB.
   - Quality: 0.75.
3. **Upload (Server Action):**
   - The Next.js server uses the **Service Account** to find/create the appropriate monthly folder.
   - Uploads the compressed file with a standardized name: `YYYY-MM-DD_Amount_Merchant.jpg`.
4. **Sheet Integration:** 
   - Appends a row to the "Finance" Google Sheet.
   - Column `Receipt_Link` will contain the direct URL to the file in Google Drive.

## 3. Roles & Permissions
- **Submitter:** Any Committee Member.
- **Auditor:** Treasurer (can see the "Claims Dashboard" with links to all Drive images).