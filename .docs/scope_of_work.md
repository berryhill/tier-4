EXHIBIT A
STATEMENT OF WORK

This Statement of Work ("SOW") incorporates the terms and provisions of the Development Agreement ("Agreement") by and between Tier4 Advisors ("Client") and Talos Technologies LLC (the "Developer") dated the __ day of 202_____. In the event of a conflict between the terms of the Agreement and any SOW, the terms of the Agreement shall control. This SOW is effective this ___ day of 202_____.

Statement of Work: Vendor Matching Engine
Client: Tier4 Intelligence
Developer: Talos Technologies LLC
Date: January 2025


1. Executive Summary
Talos Technologies LLC will design, develop, and deploy an AI-powered procurement platform consisting of two integrated components:

Vendor Matching Engine and Platform — A web-based platform enabling IT consultants to match clients with technology vendors using AI-powered search and analysis
AI Intake Agent — An intelligent intake system that conducts client discovery conversations and produces structured requirements documents

The Intake Agent serves as the client-facing front door, gathering requirements through natural conversation that feed directly into the vendor matching workflow of the Vendor Matching Engine and viewable in the platform.

NOTE:

It is understood that the underlying architecture we lay out here will grow into the client's dream of a "Tier 4" AI agent who (when coupled with Tier4's strategies and data) can "do IT Procurement better than humans." The platform described in this SOW is a step towards that goal. Next steps, such as continuous learning capabilities (of both the intake agent and agentic matching engine) are feasible but currently out of this scope; however, we (the developers) will organize the data and microservices to be extensible with this in mind. More on this later.
Project Team
Role
Person
Lead Developer, Architecture, AI Integration
Rob Rossilli
Full Stack Engineer, DevOps
Matt Berryhill
UX/UI Designer
Jessica Bond (or Client-appointed)
Junior Developer
TBD

Prior Work & Foundation
This engagement builds upon foundational work completed by Matt Roberson / T4 Intelligence, including initial system architecture, technical infrastructure decisions, backend development, and vendor data research and sourcing.


2. Engagement Structure
This project is structured in two phases:

Phase
Description
Duration
Investment
Phase 1
AI Intake Agent
4-5 weeks
$12,000-18,000 (likely lower end)
Phase 2
Vendor Matching Engine (Core Platform)
10-12 weeks
$65,000-68,000 + design


Total (agent and matching platform)
14-18 weeks
$77,000-86,000 + design


"Add-ons" are explained later in the document


3. Phase 1: AI Intake Agent
3.1 Objectives
Design, develop, and deploy an AI-powered intake agent built on voice AI platforms/libraries that conducts client discovery conversations for IT procurement consulting, producing structured requirements documents that feed into the Vendor Matching Engine. The architecture will support future integration of advisor heuristics and cross-sell/upsell suggestion capabilities (for example, Jake's intuitions on additional "upsells" or solutions that client may need).
3.2 Deliverables & Timeline
See Appendix A.1 for comprehensive deliverables breakdown.

Item
Timeline
Description
Discovery & Design
Weeks 1
Requirements gathering, team interviews, conversation flow design for all intake domains (5-6 total), voice platform evaluation and selection
Prototype Build
Weeks 2-3
Build and demo prototypes, all intake domains, deploy to dev/testing environment
Production Build
Weeks 3-4
Production deployment, all intake domains
QA & Launch
Week 4-5
Testing, launch prep, call/session logging, conversation transcripts


Total
~5 weeks


Final scope and pricing will be refined during discovery based on platform selection and Client requirements. Estimates assume 5-6 intake domains based on questionnaires provided; additional domains may increase scope. Timelines assume prompt Client feedback; delays in reviews or approvals may extend the schedule.
3.3 Scope
In Scope:

Requirements gathering and documentation
Conversation flow design for intake domains (UCaaS/CCaaS, IT Outsourcing, Security, etc.)
Voice platform evaluation and selection
Development/Production deployments (voice and text chatbot)
Integration with Vendor Matching Engine
Advisor review/approval workflow
Call/session logging

Out of Scope:

Ongoing maintenance after 30-day support period
Third-party platform costs (borne by Client)
Building voice/chat infrastructure from scratch (scope assumes use of existing platforms)
Advisor heuristics and cross-sell/upsell suggestion logic (e.g., identifying additional products/services a client may need based on conversation cues)
Self-improving agents that learn automatically from conversations (however, agents can be manually tuned based on advisor feedback and developer implementation)
Per-org/per-tenant agent provisioning (intake agents are static and shared by all orgs/tenants)

Future Extensibility: The solution will be architected to support future integration of advisor heuristics, suggestion logic, continuous learning capabilities, and custom per-org agent deployment in subsequent iterations.
3.4 Discovery
Team Interviews

Understand current intake process (how advisors conduct discovery calls today)
Identify pain points and desired improvements (ensuring specific questions are answered, etc..)
Define success criteria for the intake agent
Review all existing questionnaire templates (5-6 domains)

Technical Discovery

Evaluate voice AI platforms and libraries against requirements
Assess integration points with Vendor Matching Engine
Define output schema mapping to vendor matching system

Conversation Design

Map question logic and branching for all domains
Define handling for edge cases and ambiguous responses
Design graceful degradation (human handoff triggers)
Architect conversation flows to accommodate future advisor heuristics (Jake's upsells) and suggestion logic
3.5 Production Specifications
Note: AI interaction quality depends on platform capabilities and may require iterative tuning. Specifications below represent target behavior.

Voice Interaction Capabilities

Natural conversational flow (not robotic Q&A)
Handles interruptions and corrections
Responds appropriately to "I don't know" or partial information
Offers to repeat or clarify questions

Text Interaction Capabilities

Web-based chat interface
Same conversation logic as voice agent
Accessible via embedded widget or standalone page

Domain Coverage

All intake domains (5-6 total)
Branching logic per domain
Captures all required fields from existing questionnaires

Potential Access Methods (TBD by client)

Phone call (production phone numbers)
Google meet (agent schedules and joins meeting)
Browser-based (click-to-call from web page)
Text chatbot (web-based chat interface)

Output

Structured JSON with all captured data
Human-readable summary document (PRD/RFP format)
Confidence scores for ambiguous responses

Integration

Automatic feed into Vendor Matching Engine workflow
Advisor review/approval before vendor matching
Call/session logging and conversation transcripts
3.6 Success Criteria
Intake agent successfully conducts discovery conversations across all domains via voice and text
Both voice and text channels produce consistent, structured output
Output documents are validated for use in vendor matching workflow
Integration with Vendor Matching Engine is functional
Advisors can review and approve intake results before vendor matching (if needed)


4. Phase 2: Vendor Matching Engine
4.1 Objectives
Design, develop, and deploy a web-based platform that enables IT consultants to match their clients with technology vendors using AI-powered search and analysis.
4.2 Deliverables & Pricing
The following tables itemize all deliverables. Client may elect to remove or defer items to reduce scope and cost. See Appendix A.2 for comprehensive deliverables breakdown.

Note: AI-powered features (requirements extraction, vendor matching, enrichment) depend on underlying model capabilities and may require iterative tuning. Results will improve over time as the system is refined with real-world usage.

Tech Stack: Next.js (frontend/backend), MongoDB or Neo4j (TBD), GCP (cloud infrastructure), Kubernetes (container orchestration), GitHub Actions (CI/CD), Doppler (secrets management), OpenAI/Anthropic (LLM providers), Docker (containerization)


Core Platform
Item
Description
Authentication System
User registration with email verification, login, password recovery, account settings (email/password change, deletion)
Client Profile Management
Create/view/edit/delete client profiles with document upload
Vendor Search & Matching
Natural language queries with AI-assisted ranking, vendor detail views (certifications, services, regions, risk flags)
Admin Interface
Vendor listing/management, vendor creation with document upload and AI-assisted enrichment (Tier4 admins only)
Infrastructure & DevOps
See details below


Core Platform Total: 8-10 weeks


Infrastructure & DevOps includes:

GCP/Kubernetes configuration for dev and production environments
CI/CD pipeline with automated testing and deployment
Database setup (MongoDB or Neo4j, TBD) with automated backup configuration
Monitoring & observability (logging, alerting, basic dashboards)
DNS configuration and initial external service API keys

Ongoing infrastructure management (monitoring, updates, troubleshooting) is Client's responsibility after handoff. Comprehensive documentation will be provided to support self-maintenance. If Client prefers Developer to handle ongoing maintenance, a separate maintenance agreement can be provided upon request.


Optional / Deferrable
Item
Description
Duration
Price
Marketing Site


1 week
$1,000-4,000 (depending on designs)
- Landing/Home Page
Hero, value proposition, features overview, CTAs




- Pricing Page
Pricing tiers, feature comparison, signup CTAs




- About/Company Page
Company info, team, mission




- Privacy Policy
Legal language provided by Client




- Terms of Use
Legal language provided by Client






Note: Branding assets (logos, colors), website copy, and design assets are Client's responsibility or handled by Client's designer (e.g., Jessica Bond) and are not included in the estimates above.


Pricing Summary
Category
Subtotal
Core Platform (includes Infrastructure)
$64,000
Optional / Deferrable
$1,000-4,000
Total (all items)
$65,000-68,000


Minimum Viable Build (Core only - no marketing pages): $64,000


4.3 Scope Notes
Included in pricing above:

Responsive design for desktop, tablet, and mobile
QA testing across standard devices (iPhone, Android, Mac, Windows) and browsers (Chrome, Safari); assumes devices and browsers are reasonably up to date
SOC 2 readiness (architected for compliance; certification is Client responsibility if desired)
Post-launch bug fix period (30 calendar days)
Documentation (deployment, environment configuration, maintenance guide)
Client access to source code repository and infrastructure dashboards

Design Prerequisite (not included in pricing): Wireframes and low-fidelity designs are required before development begins. These serve as the spec that development will be built against. Client may:

Provide their own wireframes/designs, or
Use Developer's designer (Jessica Bond or equivalent) at $85/hr

Design work will be scoped and estimated separately during project kickoff.

Out of Scope:

Ongoing maintenance, monitoring, and troubleshooting beyond the 30-day post-launch support period
Multi-user shared accounts (multiple advisors sharing clients)
API key rotation schedule and ongoing responsibility
Long-term database backup monitoring and management
Privacy Policy & Terms of Use legal language (provided by Client)
Vendor data sourcing, web scraping, research, and curation (Client responsibility)
External users/vendors updating or adding vendor data (admin access is Tier4 only)
AI Training Feedback Environment (advisor interface for reviewing/re-ranking AI recommendations, feedback capture, training data export)
Self-improving matching algorithms that learn automatically from usage

Future Extensibility: The platform will be architected to support future integration of AI training feedback loops, continuous learning, advanced optimization (e.g., GEPA-based), and external vendor self-service portals (allowing vendors to update their own profiles) in subsequent iterations.
4.4 Timeline
Timeline scales with selected scope:

Scope
Duration
Vendor Matching Engine Platform Build ($65K-68K)
10-12 weeks


Phase
Duration
Wireframes & Low-Fi Designs
2-3 weeks (prerequisite, not included in fixed fee)
Core Development
10-12 weeks
QA & Launch Prep
1-2 weeks
Bug Fix Period
30 days post-launch

4.5 Critical Milestones
Design approval: wireframes + low-fi designs (prerequisite before development begins)
Dev environment setup
Auth system complete
Client management features complete
Vendor search features complete
Admin interface complete
(If selected) Optional features complete
QA testing complete
Internal beta launch (Tier4 team testing)
Production beta launch
4.6 AI Optimization Approach
Platform launches with baseline AI optimization (BootstrapFewShot) for vendor matching. Initial matching quality will vary; iterative refinement is expected as the system encounters real-world queries. Manual tuning will be supported based on advisor feedback.

Training Data Requirement: Vendor matching results are inherently opinionated—the "best" vendor for a given set of requirements depends on Tier4's expertise and judgment. To achieve accurate matching, training data is required (e.g., example queries paired with ideal vendor rankings). Client is responsible for providing or curating this training data in the format specified by Developer. Without sufficient training data, matching quality will rely on general-purpose AI reasoning and may not reflect Tier4's domain expertise.

Out of Scope: Training environment infrastructure and continuous learning systems (where the model automatically improves from usage) are not included in this engagement. These can be added in future iterations.

Advanced optimization capabilities (AI Training Feedback Environment, GEPA-based learning) can be added in future iterations as described in the Future Extensibility note above.
4.7 Vendor Data Seeding
Building the vendor enrichment tools (admin interface) is included in the pricing above. Developer will provide initial training on these tools.

Client Responsibility: Populating the vendor database is the responsibility of Client, including:

Researching and sourcing vendor information
Web scraping and data collection
Curating and structuring vendor data in a consistent format
Uploading documents and running enrichment via admin tools
Reviewing and validating AI-enriched results

Client will provide vendor data in an agreed-upon structure/format. If Client requests Developer to perform data curation work, it will be billed at the hourly rate specified in Payment Terms.

Future Extensibility: Automated vendor scraping tools (to programmatically collect and update vendor information from websites) can be added in future iterations.

4.8 Success Criteria
                                                                                                                                                
  - Users can register, verify email, login, and manage their accounts                                                                          
  - Organizations can be created with proper data isolation (Org A cannot see Org B's data)                                                     
  - Users can invite team members and manage organization membership                                                                            
  - Client profiles can be created, viewed, edited, and deleted with document upload                                                            
  - Vendor search returns relevant results using natural language queries                                                                       
  - AI matching produces ranked vendor recommendations with match scores and explanations                                                       
  - Side-by-side vendor comparison is functional                                                                                                
  - Export to PDF and CSV works for search results                                                                                              
  - Admin interface allows Tier4 admins to create, edit, and manage vendors                                                                     
  - AI-assisted vendor enrichment from uploaded documents is functional                                                                         
  - Intake agent data flows into VME and is viewable in client profiles                                                                         
  - Platform is responsive across desktop, tablet, and mobile                                                                                   
  - Platform passes QA testing on standard browsers (Chrome, Safari) and devices (iPhone, Android, Mac, Windows)                                
  - Application is deployed to production with CI/CD pipeline operational                                                                       
  - Monitoring, logging, and alerting are configured and functional   



5. Payment Terms
Milestone-Based Payment Schedule
#
Milestone
Trigger
%
1
Signed agreement
Contract execution
15%
2
Intake agent demo
Working prototype reviewed (voice + text)
15%
3
Intake agent live
Production deployment, collecting data
15%
4
VME alpha
Auth + client management + vendor search functional on dev
25%
5
VME complete
All features, intake agent integrated, QA passed, deployed to production
30%


Percentages are applied to the total agreed engagement value.
Additional Costs (Not Included in Milestone Payments)
UX/UI Design: If Client chooses to use Developer's designer for wireframes and low-fidelity designs, work is billed at $85/hr (designer's rate, passed through with no markup). Client may alternatively provide their own designs.

Reimbursables: Third-party service costs borne by Client including voice platform fees, telephony, APIs, GCP hosting (monthly), email service, etc.
Out-of-Scope Work
Any work requested by Client that falls outside the scope defined in this SOW will be billed at $120/hr via Change Order.


6. Client Responsibilities
General
Attend weekly status meetings
Provide timely feedback on deliverables (delays may affect timeline)
Review and approve deliverables within 7 business days
Phase 1 Specific
Provide access to all existing questionnaire templates
Make team members available for discovery interviews
Provide example intake call recordings or transcripts (if available)
Provide sample PRD/RFP output documents (desired format)
Review and provide feedback on conversation flows
Define success criteria for intake agent
Define success criteria for vendor matching engine functionality
Phase 2 Specific
Provide branding assets (logo, colors) before marketing page finalization
Provide wireframes and low-fi designs prior to development (or engage Developer's designer)
Provide access to required accounts (domain registrar, GCP billing)
Provide billing information for GCP infrastructure costs - and all other ancillary costs (ai tokens, doppler, etc..)
Collaborate on vendor schema definition during development
Review and approve designs within 7 business days
Source, curate, and provide vendor data in agreed-upon format for database seeding
Provide or curate training data for vendor matching (example queries with ideal vendor rankings) in format specified by Developer


7. Communication & Reporting
Weekly Status Calls
Developer and Client will hold weekly calls to:

Demonstrate progress on current work
Gather feedback and answer questions
Discuss next steps and priorities
Ongoing Visibility
All work will be visible and reviewable at any time via project management tools (e.g., GitHub Issues, Trello, or similar platform agreed upon by both parties).
Written Reports
Formal written progress reports will be provided upon Client request.


8. Assumptions
Timeline assumes timely Client feedback
Voice AI platform/library meets technical requirements (validated in Phase 1)
AI voice/text interaction quality is dependent on selected platform and may vary; iterative refinement is expected
Vendor schema will be defined collaboratively during development
Third-party service costs (OpenAI, cloud hosting, email service) are borne by Client
GCP is the designated cloud provider
Open Questions (TBD)
Billing Model: Subscription tiers, usage-based, or freemium?
Usage Limits: Limits on searches, clients, or proposals per user?
Branding: Platform name, logo, and color palette?
Proposal Format: PDF, Word document, or in-app view?
Refund Policy: How to handle users who want a refund?
etc…


9. Acceptance Testing
Developer will perform thorough testing across all features and user flows
Upon delivery of each major milestone, Client has 7 business days to review and provide written acceptance or rejection with specific deficiencies
If no response is received within 7 business days, the milestone is deemed accepted
Developer does not warrant that the Software will be entirely free from defects or operate without interruption. Developer will use commercially reasonable efforts to correct material defects identified during the acceptance period.


10. Investment Summary
Phase 1: AI Intake Agent
Configuration
Investment
Range
$12,000 - $18,000 (likely lower end)


Final scope refined during discovery.
Phase 2: Vendor Matching Engine
Configuration
Includes
Total
Full Build
Core + All Optional
$65,000-68,000
Core Build
Core only
$64,000
Custom
Core + selected options
$64,000 + selected

Full Engagement Summary
Phase
Description
Investment
1
AI Intake Agent
$12,000 - $18,000
2
Vendor Matching Engine (see options above)
$65,000 - $68,000


Range
$77,000 - $86,000


Plus: UX/UI design @ $85/hr (hours TBD).


Appendix A: Comprehensive Deliverables Breakdown
This appendix provides a detailed breakdown of all deliverables included in the engagement.


A.1 Phase 1: AI Intake Agent
Discovery & Requirements
Stakeholder interviews with advisory team
Review of existing questionnaire templates (all domains)
Success criteria definition
Existing platform research and evaluations
Conversation Design
Conversation flow architecture
Domain-specific flows:
UCaaS/CCaaS
IT Outsourcing
Security
(additional domains as identified)
Branching logic per domain
Required vs optional field mapping
Edge case handling (ambiguous answers, refusals, "I don't know")
Graceful degradation / human handoff triggers
Clarification and rephrasing logic
Conversation state management
Voice Agent
Voice platform integration
Natural conversational flow (not robotic Q&A)
Interruption handling
Speech-to-text accuracy tuning
Text-to-speech voice selection
Phone number provisioning (production)
Inbound call routing
Call recording (if required)
Text/Chat Agent
Web-based chat interface
Identical conversation logic to voice
Standalone page version
Mobile-responsive design
Output Generation
Structured JSON schema for all captured data
Human-readable summary document (PRD/RFP format)
Confidence scores for ambiguous responses
Missing/incomplete data flags
Field validation and normalization
Vendor Matching Engine Integration
API connection to Vendor Matching Engine
Secure data handoff
Advisor review queue
Approval/rejection workflow
Edit capability before matching
Status tracking (draft, pending review, approved)
Logging
Call/session logging
Conversation transcripts
Basic metrics (total calls, completed vs abandoned)


A.2 Phase 2: Vendor Matching Engine
Authentication & Authorization
User Registration & Login

User registration with email/password
Email verification flow (send, verify, resend)
Login / logout
Password reset (forgot password flow)
Session management (secure tokens)

Account Management

Account settings page
Change email
Change password
Delete account

Multi-Tenant Architecture

Organization creation
Organization settings
Organization-level data isolation (Org A cannot see Org B's data)

Role-Based Access Control (RBAC)

Admin role
Member role
Permission definitions per role

Organization Membership

Invite users via email
Accept/decline invitations
Remove members
Transfer ownership

Security

Password hashing
Brute force protection
Session invalidation
Secure cookie handling
SOC 2 readiness (architected for compliance; certification is Client responsibility)


Client Management
Client List View

Search by name/keyword
Filter by status, date, domain
Sort options
Pagination

Create Client Profile

Manual entry form
Required vs optional fields
Validation

View Client Profile

Summary view
Full details view
Linked intake sessions
Matching history

Edit Client Profile

Field-level editing
Change tracking

Delete Client Profile

Soft delete vs hard delete
Confirmation flow

Document Management

Upload documents (must follow agreed-upon template/structure; arbitrary document parsing is out of scope)
Document preview

Future: AI-powered requirements extraction from uploaded documents can be added in subsequent iterations.

Status Tracking

Draft, active, archived
Status change workflow


Vendor Database (Data Model)
Core Vendor Fields

Company name, description, website
Logo/branding
Service categories
Geographic coverage (regions, countries)
Company size / employee count
Year founded
Certifications and compliance
Pricing model / tiers
Contract terms
Support offerings
Risk flags / concerns
Strengths / differentiators
Contact information

Data Management

Custom/extensible fields
Vendor status (active, inactive, pending review)


Vendor Management (Tier4 Admin Only)
Admin Dashboard

Overview metrics
Quick actions
Recent activity

Vendor List View

Search, filter, sort
Bulk selection
Pagination

Create Vendor

Manual entry form
Document upload
AI-assisted enrichment from documents
Field validation

View Vendor

Full profile view
Usage statistics (how often matched)

Edit Vendor

Field-level editing

Delete Vendor

Soft delete

Data Quality Tools

Duplicate detection
Validation rules


Vendor Search & Matching
Search Interface

Natural language query input
Guided search / filters
Search suggestions / autocomplete

AI Matching Engine

Query understanding
Requirement extraction
Vendor scoring algorithm
Relevance ranking

Results Display

Ranked list view
Match score / confidence
Key match factors highlighted
Quick preview

Vendor Detail View

Full vendor profile
Match explanation
Comparison to requirements

Comparison

Side-by-side comparison
Feature matrix
Strengths/weaknesses summary

Export & Reporting

Export to PDF
Export to CSV


User Interface & Experience
Design System

Component library
Consistent styling
Reusable patterns

Responsive Design

Desktop layouts
Tablet layouts
Mobile layouts

Navigation

Primary navigation
Breadcrumbs
Context menus

Dashboard / Home Page

Recent activity
Quick actions
Key metrics

Form Components

Input validation
Error messaging
Help text / tooltips
Auto-save (where appropriate)

Data Tables

Sorting
Filtering
Export

Loading States

Skeleton screens
Progress indicators
Optimistic updates

Empty States

First-time user guidance
No results messaging
Call-to-action prompts

Error Handling

User-friendly error messages
Recovery suggestions
Error reporting


Backend / API
API Architecture

REST API design
Resource-based routes
Consistent naming conventions
Versioning strategy

Request Handling

Input validation
Sanitization
Rate limiting

Response Formatting

Consistent JSON structure
Error response format
Pagination metadata

Authentication Middleware

Token validation
Permission checking
Org context

Background Jobs

AI processing queues
Document processing
Email sending

Logging

Request/response logging
Error logging
Audit trail


Database
Database (MongoDB or Neo4j, TBD)

Schema design
Data modeling
Relationships
Properties/fields

Performance & Integrity

Indexes for query performance
Constraints for data integrity
Query optimization
Migration strategy


AI / ML Components
LLM Integration

OpenAI/Anthropic integration
API key management
Cost monitoring

Prompt Engineering

Requirements extraction prompts
Vendor enrichment prompts
Matching/ranking prompts

Processing Pipeline

Context management
Token optimization
Error handling / fallbacks
Confidence scoring
Response parsing and validation


Infrastructure & DevOps
Cloud Infrastructure (GCP)

Project setup
IAM / service accounts
VPC / networking
Resource organization

Kubernetes

Cluster provisioning (dev)
Cluster provisioning (prod)
Namespace organization
Resource limits / quotas
Horizontal pod autoscaling
Health checks / probes

Containerization

Dockerfile for each service
Image optimization
Registry setup (GCR/Artifact Registry)

CI/CD (GitHub Actions)

Repository setup
Branch protection rules
Pull request workflows
Automated testing pipeline
Build pipeline
Deployment pipeline (dev)
Deployment pipeline (prod)
Environment promotion
Rollback procedures

Database Operations

Database provisioning (MongoDB or Neo4j, TBD)
Backup automation (daily)
Backup retention policy
Restore procedures
Disaster recovery plan

Secrets Management (Doppler)

API keys
Database credentials
Service account keys
Environment-based secret injection

Monitoring & Observability

Application logging
Log aggregation
Error tracking
Performance monitoring
Uptime monitoring
Alerting rules
Dashboards

DNS & SSL

Domain configuration
SSL certificate provisioning
Certificate auto-renewal

External Service Setup

OpenAI/Anthropic API keys
Email service (SendGrid, etc.)
File storage (GCS)


Security
Input validation (all endpoints)
Output encoding (XSS prevention)
CSRF protection
Injection prevention
Rate limiting
API authentication
Data encryption in transit (TLS)
Data encryption at rest
Secure headers (HSTS, CSP, etc.)
Audit logging
SOC 2 readiness (architected for compliance; certification is Client responsibility)


Testing
Unit tests (critical paths)
Integration tests (API)
End-to-end tests (key workflows)
Manual QA testing
Cross-browser testing
Mobile responsiveness testing
Performance testing (basic)
Security testing (basic)


Documentation
Deployment guide
Environment configuration guide
API documentation
Admin user guide
Troubleshooting runbook
Architecture overview


A.3 Optional Add-Ons
Marketing Site
Landing / home page
Pricing page
About page
Privacy policy page
Terms of use page
Proposal Document Generation
Comparison proposal documents from vendor matches
PDF export
