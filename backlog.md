# 🗂️ CandidateMatch Product Backlog

This backlog includes epics and associated user stories categorized by core product functionality.

---

## 🧭 Epic 1: User Onboarding & Profile Setup

### User Story 1.1: Survey Completion
**As a** new user  
**I want to** complete a survey ranking political issues by importance  
**So that** the app can generate a profile that reflects my values.

**Acceptance Criteria:**
- User sees a list of 10–15 political issues.
- User can rank or rate importance on a scale.
- Responses are stored locally or in a secure database.

---

### User Story 1.2: Stance Deep-Dive
**As a** user  
**I want to** provide additional context on my stance (e.g., text input or sliders)  
**So that** the system can better personalize candidate matching.

**Acceptance Criteria:**
- Optional follow-up for top 3 ranked issues.
- Interface supports sliders or free text per issue.

---

### User Story 1.3: Anonymous Access
**As a** privacy-focused user  
**I want to** use the application without creating an account  
**So that** I can explore matches without sharing personal data.

**Acceptance Criteria:**
- No email/login required.
- A session-based anonymous ID is generated for matching.

---

## 🔍 Epic 2: Candidate Data Management

### User Story 2.1: Candidate Profile Display
**As a** voter  
**I want to** view clear, summarized profiles of each candidate  
**So that** I can understand their background, policies, and affiliations.

**Acceptance Criteria:**
- Displays name, office, party, photo, and bio.
- Links to official website and filings.

---

### User Story 2.2: Policy Position Mapping
**As a** system  
**I want to** extract candidate issue stances from verified data  
**So that** I can display relevant issue-aligned views.

**Acceptance Criteria:**
- Use NLP to extract positions from debate transcripts, press releases, voting records.
- Attach citations and confidence scores.

---

### User Story 2.3: Update Candidate Database
**As a** backend admin  
**I want to** periodically refresh candidate profiles  
**So that** voters see up-to-date and accurate information.

**Acceptance Criteria:**
- Data updated weekly or via API triggers.
- Logs maintained for each update.

---

## 🧠 Epic 3: Matching Algorithm & Score Engine

### User Story 3.1: Compute Alignment Scores
**As a** voter  
**I want to** receive a ranked list of candidates that align with my views  
**So that** I can make an informed voting decision.

**Acceptance Criteria:**
- Match score calculated using weighted similarity between user preferences and candidate stances.
- Explanation tooltip available for score derivation.

---

### User Story 3.2: Visualize Matching Results
**As a** user  
**I want to** see visual representations of my match breakdown  
**So that** I can understand where alignment occurs or doesn’t.

**Acceptance Criteria:**
- Display charts (bar or radar) of match by issue.
- Offer toggle to compare top 2–3 candidates.

---

## 📊 Epic 4: Compare & Engage

### User Story 4.1: Candidate Comparison Tool
**As a** voter  
**I want to** compare multiple candidates side-by-side  
**So that** I can easily contrast their positions.

**Acceptance Criteria:**
- Select up to 3 candidates.
- Issue-by-issue comparison in table or card format.

---

### User Story 4.2: Voter Action Hub
**As a** user  
**I want to** see links to voter registration and ballot info  
**So that** I can take next steps after reviewing matches.

**Acceptance Criteria:**
- Integrate with Vote.org, local election sites, etc.
- Localize links by ZIP or IP.

---

### User Story 4.3: Share My Results
**As a** user  
**I want to** share my match results on social media  
**So that** I can spark civic engagement in my network.

**Acceptance Criteria:**
- Share card image with match summary.
- Allow customization before sharing.

---

## 🔒 Epic 5: Trust, Feedback & Transparency

### User Story 5.1: See Sources and Citations
**As a** user  
**I want to** verify where candidate statements come from  
**So that** I can trust the information shown.

**Acceptance Criteria:**
- Each issue stance includes source URL or document.
- “Unverifiable” flags for unclear data.

---

### User Story 5.2: Submit Feedback
**As a** user  
**I want to** flag incorrect or biased information  
**So that** the platform can improve accuracy.

**Acceptance Criteria:**
- Simple feedback form tied to candidate or match result.
- Feedback stored with optional email for follow-up.

---

## ⚙️ Epic 6: Admin & CMS Tools

### User Story 6.1: Manage Issues List
**As a** content editor  
**I want to** update the list of issues or keywords  
**So that** the system stays relevant to public discourse.

---

### User Story 6.2: View Data Quality Reports
**As a** system admin  
**I want to** monitor data confidence and missing stances  
**So that** I can prioritize manual review where needed.

---

## 🧪 Epic 7: QA & Testing

### User Story 7.1: Test Candidate Match Accuracy
**As a** QA engineer  
**I want to** run match simulations against test users  
**So that** I can validate the correctness of the algorithm.

---

### User Story 7.2: Accessibility Testing
**As a** QA tester  
**I want to** test the site with screen readers and keyboard navigation  
**So that** it’s usable for everyone.

---

## 🧰 Epic 8: Infrastructure & Deployment

### User Story 8.1: Secure Hosting
**As a** devops engineer  
**I want to** host the app on a secure cloud platform  
**So that** user data is protected and performance is stable.

---

### User Story 8.2: Analytics Integration
**As a** product manager  
**I want to** track usage stats like quiz completion and shares  
**So that** I can optimize UX and outreach.

---

## 📅 Future Enhancements (Backlog Candidates)

- Enable candidate login and profile verification.
- Personalized notifications about debates or voter deadlines.
- Support for ranked-choice voting.
- Gamified quiz interface to boost engagement.

