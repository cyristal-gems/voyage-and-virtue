# Voyage & Virtue Website Setup

## The Gallery Guards

The Voyage & Virtue site is a deliberately staged honeypot web application disguised as a luxury art dealer and travel service. It is designed to attract attackers, entice them into interacting with sensitive-looking content, and silently trigger Canary tokens.

1. **Landing Page (`index.html`)**  
   **Theme:** Sets the luxury “art + travel” vibe and routes visitors to the functional areas.  
   **Defensive purpose:** Looks legitimate to scanners and humans and is intentionally “clean”—no direct downloads here. It funnels traffic into the tokened pages (guest/employee/login).

2. **About (`about.html`)**  
   **Theme:** Credibility page that explains the gallery/travel consultancy story and values.  
   **Defensive purpose:** Keeps the site from feeling like a thin trap.

3. **Login Portal (`login.html`)**  
   **Theme:** “VIP Access” login page.  
   **Key features:**  
   a) Employee Login Form → tied to a Canary token.  
   b) Guest Login Form → tied to a Canary token.  
   c) Login Success Trap → even a fake “success” is tokened.  
   **Defensive purpose:** Encourages brute-force or credential-stuffing attempts. Every attempt is logged as an initial access technique (T1190).

4. **Guest Portal (`guest.html`)**  
   **Theme:** A polished travel/collector experience highlighting exotic destinations and art exhibitions.  
   **Key features:**  
   a) VIP Itinerary – Marrakech & Cairo → download link, tied to `CANARY_URL_ITINERARY`.  
   b) Private Viewing Protocols → access instructions, tokened via `CANARY_URL_GUEST_PROTOCOLS`.  
   c) Collector Contact List (Redacted) → download link, tokened via `CANARY_URL_CONTACTS`.  
   d) Art Shipment Manifest Preview → another bait document, tokened trigger.  
   **Defensive purpose:** Simulates an enticing front-end with travel and art “assets.” Any download or interaction quietly sets off alerts.

5. **Employee Portal (`employee.html`)**  
   **Theme:** An internal gallery staff portal styled as a professional operations dashboard. It surfaces what appear to be privileged resources needed by employees to manage guests, shipments, and vendors.  
   **Key features:**  
   a) VIP Guest List (OFFICIAL) → download link, tokened via `CANARY_URL_VIP_GUESTLIST`.  
   b) Collector Contacts (OFFICIAL) → download link, tokened via `CANARY_URL_COLLECTOR_CONTACTS`.  
   c) Gallery Access Logs → download link, tokened via `CANARY_URL_ACCESS_LOGS`.  
   d) Incident Runbooks → download link, tokened via `CANARY_URL_INCIDENT_RUNBOOKS`.  
   e) Shipment Manifests → download link, tokened via `CANARY_URL_SHIPMENT_MANIFESTS`.  
   f) Vendor Registry → download link, tokened via `CANARY_URL_VENDOR_REGISTRY`.  
   **Defensive purpose:** Presents itself as a sensitive back-office hub for gallery operations. Each file is enticing bait for attackers, but in reality every download is a Canary token trigger. Access attempts generate alerts to CloudWatch/SNS/SIEM, enabling rapid detection of intrusions.

6. **News (`news.html`)**  
   **Theme:** A “Freshness” page that mimics press/updates.  
   **Defensive purpose:** Supports realism and provides an optional place to add tokened “press kits” or PDFs later.
