# StealthPlatform

Private, hardened Desktop-as-a-Service (DaaS) reference workspace.

Components:
- 1_Orchestrator_API/  — ASP.NET Core 8.0 Web API (VM lifecycle, token issuance, region/gateway assignment)
- 2_Billing_Worker/    — Python 3.11 daemon (per-minute reconciler, DECIMAL(12,6) ledger writes)
- 3_Client_Portal/     — React + TypeScript frontend (prepaid wallet, region selector, Guacamole embed)

See ARCHITECTURE.md for system design, privacy hardening, and billing/network interactions.

Operational documentation:
- `operations/guacamole_mapping.md` — Guacamole session binding, short-lived token workflow, and single-session rules.
- `operations/windows_template_hardening.md` — Windows Golden Master hardening, telemetry lockdown, timezone sync, and snapshot hygiene.
- `operations/windows_network_proxy.md` — Exact Windows DNS and residential proxy network isolation configuration.
- `operations/deployment_guide.md` — Production launch checklist for Proxmox, backend deployment, Guacamole integration, and operational controls.
- `operations/enterprise_service_architecture.md` — High-value safe browser, proxy brokerage, and telephony service architecture.
- `operations/internet_access_marketplace.md` — Global internet access brokerage and connectivity service design.
- `operations/ban_proof_checklist.md` — Practical ban-proof and anti-fraud checklist for pixel-only browsing and proxy sessions.
- `operations/antidetect_browser_architecture.md` — Full secure browser architecture and enterprise antidetect platform design.
- `operations/complete_ecosystem_architecture.md` — Unified ecosystem design with client access, services, and product flow.
- `CLIENT_SERVICE_CENTER.md` — Client-facing service architecture, portal connection flow, and user access path.
