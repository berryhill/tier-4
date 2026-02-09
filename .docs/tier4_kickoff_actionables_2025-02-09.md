# Tier 4 Kickoff Call - Action Items
**Date:** February 9, 2025  
**Recording:** [Fathom Recording (31 mins)](https://fathom.video/share/ba3BX97sqHMjRTpPzjGSLTnD_VyFxHjk)

---

## Immediate Action Items for Tier 4

### 1. Add Matt Berryhill to Slack
- **Email:** `matt.pineappleworkshop@gmail.com`
- **Action:** Add to Tier 4 Slack workspace and create dedicated project channel

### 2. Create Admin Email for Upstream Accounts
- **Purpose:** Single admin email for all infrastructure and third-party service accounts
- **Services needing admin access:**
  - GCP (Google Cloud Platform) - infrastructure
  - Doppler (secrets management)

### 3. Confirm Weekly Meeting Time
- **Proposed:** Tuesdays at 2:30 PM EST (11:30 AM PST)
- **Status:** Awaiting confirmation

### 4. Formalize Points of Contact

| Role | Name | Contact |
|------|------|---------|
| **Tier 4 Primary POC** | Nate Sherrill | (email TBD) |
| **Tier 4 CTO** | Eric | (email TBD - Nate to provide) |
| **Tier 4 Finance** | Jake | (handled payment) |
| **Tier 4 Technical** | Matt Robertson | (limited involvement, but looped in) |
| **Developer Lead** | Rob Rossilli | (phone shared with Nate) |
| **Developer Full Stack/DevOps** | Matt Berryhill | matt.pineappleworkshop@gmail.com |

---

## Summary of Decisions Made

1. **Infrastructure Provider:** GCP (pending final confirmation from Eric)
2. **Communication Channel:** Slack (async) + Weekly Tuesday calls (sync)
3. **Progress Tracking:** GitHub (technical tasks) + Trello (high-level)
4. **Development Start:** Pending payment receipt confirmation

---

## Next Steps

Once the above items are complete, the developer team will:

### Infrastructure Setup
1. Set up GitHub organization and add Tier 4 team members
2. Create GitHub project board for task tracking
3. Configure GCP project structure (dev + prod environments)
4. Set up Kubernetes clusters for container orchestration
5. Configure CI/CD pipeline with GitHub Actions
6. Set up Doppler for secrets management
7. Configure monitoring and observability (logging, alerting)

### Development Kickoff
1. Begin Phase 1 research on AI intake agent platforms
2. Evaluate voice AI SDKs and present options with cost/benefit analysis
3. Start backend architecture for vendor matching engine
4. Define database schema (MongoDB or Neo4j - TBD)
5. Build vendor data ingestion pipeline - enable Tier 4 to efficiently communicate and ingest vendor information

---

## Notes from Call

- Nate emphasized proactive communication - "please stay on top of me"
- Eric is accessible for DNS/infrastructure coordination (previously worked together)
- **UX/UI Design:** Tier 4 to determine their preferred approach for design/wireframes. Rob and Matt are technical specialists, not UX/UI designers - recommend engaging a specialist in that field. Open to whatever approach Tier 4 decides.
- Vendor data schema discussion needed - rough list of fields to capture per vendor
- Platform naming decision pending - important to establish early for consistent documentation
