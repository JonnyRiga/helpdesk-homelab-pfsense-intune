# Helpdesk Homelab (pfSense, Windows Domain, Intune MDM)

A self-built virtual homelab that reproduces real **Level 1 & 2 IT support** work from end to end: identity and access management in Active Directory, DNS/DHCP and connectivity troubleshooting, Group Policy, remote support, and **Microsoft Intune (MDM)** device enrolment with compliance reporting. Every issue is worked and written up as a **ticket-style runbook**.

**Stack:** VirtualBox, pfSense, Windows Server (AD DS, DNS), Windows 10 client, Microsoft Intune / Entra ID, PowerShell.

> Personal lab built to practice the day-to-day workflow of a desktop/service-desk role: triage, reproduce, isolate, resolve, document, and escalate.

**Recruiters:** a short guided tour with the key screenshots and runbooks is here → [docs/00-overview/recruiter-quick-links.md](docs/00-overview/recruiter-quick-links.md).

## What I built
- **pfSense** firewall/router providing a WAN/LAN boundary and DHCP on the internal lab LAN
- **Windows Server domain controller** with AD DS and DNS (`lab.local`)
- **Windows 10 client** joined to the domain
- **Microsoft Intune (MDM)** enrolment of the domain-joined client, with a compliance policy and reporting validation
- **Ticket-style runbooks** documenting each issue: symptoms, diagnosis, resolution, and escalation cues

## Skills demonstrated (mapped to real service-desk duties)
- **Level 1 & 2 support:** triage, reproduce, resolve, document, and escalate
- **Identity & access (AD / Entra ID):** users and security groups, password resets/unlocks, permission and login troubleshooting
- **Device management (Intune / MDM):** enrolment, compliance policy, reporting
- **Networking:** DNS, DHCP, TCP/IP, connectivity diagnosis (pfSense WAN/LAN)
- **Remote support:** RDP and endpoint firewall rules
- **Endpoint config:** Group Policy (GPO) for workstation and user settings
- **Documentation:** clear, repeatable runbooks and knowledge-base notes

## Architecture
- Overview: [docs/00-overview/architecture.md](docs/00-overview/architecture.md)
- IP plan: [docs/00-overview/ip-plan.md](docs/00-overview/ip-plan.md)
- VM inventory: [docs/00-overview/vm-inventory.md](docs/00-overview/vm-inventory.md)
- Network diagram: [docs/00-overview/network-diagram.md](docs/00-overview/network-diagram.md)

## Build guide
1. VirtualBox networks: [docs/01-build-guide/01-virtualbox-networks.md](docs/01-build-guide/01-virtualbox-networks.md)
2. pfSense install: [docs/01-build-guide/02-pfsense-install.md](docs/01-build-guide/02-pfsense-install.md)
3. Windows Server AD DS and DNS: [docs/01-build-guide/03-windows-server-ad.md](docs/01-build-guide/03-windows-server-ad.md)
4. Windows 10 domain join: [docs/01-build-guide/04-windows10-domain-join.md](docs/01-build-guide/04-windows10-domain-join.md)
5. Intune MDM enrolment: [docs/01-build-guide/05-intune-mdm-enrollment.md](docs/01-build-guide/05-intune-mdm-enrollment.md)

## Runbooks (ticket-style)
- Index: [docs/02-runbooks/README.md](docs/02-runbooks/README.md)
- [Ticket 001: Domain login failure](docs/02-runbooks/ticket-001-domain-login-failure.md)
- [Ticket 005: Intune device non-compliant](docs/02-runbooks/ticket-005-intune-noncompliant.md)

## Proof (screenshots)
See [docs/03-proof/proof-checklist.md](docs/03-proof/proof-checklist.md) and `docs/03-proof/screenshots/`.
