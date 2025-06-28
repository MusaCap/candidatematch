# 🗳️ PRD: CandidateMatch – Personalized Candidate Discovery

## Overview

**Product Name:** CandidateMatch  
**Purpose:** Help voters easily identify and understand which election candidates best align with their personal views on key issues.  
**Target Users:**  
- First-time voters  
- Undecided voters  
- Politically engaged citizens  
- Media outlets and civic education groups  

## Goals

- Increase voter participation and confidence in elections.
- Simplify candidate comparison based on personal values.
- Ensure data transparency and neutrality.
- Provide accessible, easy-to-understand information across platforms.

---

## Key Features

### 1. User Onboarding & Issue Prioritization
- **Survey UI**: Users complete a short quiz ranking the importance of key topics (e.g., climate change, healthcare, immigration, economy).
- **Optional Deep-Dive**: Users can elaborate their stance with short-answer questions or sliders on subtopics.
- **Personal Profile Generation**: The app generates a voter values profile stored locally or in a secure cloud account.

### 2. Candidate Database
- **Aggregated Profiles**: Pulled from public campaign data, debates, interviews, voting records, and third-party databases (e.g., BallotReady, OpenSecrets).
- **Stance Mapping Engine**: Uses NLP to tag candidate views and statements by topic with confidence scores.
- **Fact-Checking Layer**: Third-party verified sources are cited; unclear positions are flagged for user awareness.

### 3. Matching Algorithm
- **Weighted Match Score**: Each candidate is scored based on alignment with user’s topic priorities and stances.
- **Transparency Panel**: Users can inspect why a candidate scored high or low with interactive charts.

### 4. Explore & Compare
- **Visual Cards**: For each matched candidate, show a snapshot: bio, major issues, notable quotes, donor summary, endorsements.
- **Side-by-Side Comparison**: Users can pick 2–3 candidates and view detailed policy comparisons.

### 5. Engagement & Sharing
- **Voter Action Hub**: Includes links to registration, polling location lookups, and ballot previews.
- **Social Sharing**: Share results to raise awareness (“I matched with __ on 8 out of 10 issues”).
- **Feedback Loop**: Users can flag inconsistencies or request deeper clarification on issues.

---

## Technical Requirements

### Backend
- **Data Sources**: APIs from VoteSmart, OpenSecrets, GovTrack, BallotReady, and manual scraping pipelines.
- **NLP Pipeline**: To extract topic stances and candidate sentiment from open-text sources.
- **Matching Engine**: Weighted cosine similarity or custom distance metric with tunable parameters.

### Frontend
- **Responsive Web App** (React, Tailwind, Typescript) and optional **mobile-first** layout.
- **Interactive UI** for onboarding and comparisons (e.g., D3.js or Recharts for data viz).
- **Accessibility**: WCAG 2.1 compliance for inclusive access.

---

## Privacy & Trust

- **Data Usage Transparency**: User data is never sold; profiles are private by default.
- **Anonymity Option**: Full access to matching engine without requiring signup.
- **Audit Logs**: Open-source logs for transparency in stance scoring and updates.

---

## Success Metrics

- % of users who complete the onboarding quiz
- % of users who click through to register to vote
- Time spent comparing candidates
- Number of social shares or referrals
- User feedback on match accuracy and satisfaction

---

## Timeline

| Phase        | Milestone                                 | Timeline   |
|--------------|--------------------------------------------|------------|
| Discovery    | Finalize requirements, validate data sources | Week 1–2  |
| Design       | UX/UI wireframes, data flow mapping         | Week 3–4  |
| MVP Build    | Survey UI, candidate ingest, basic matching | Week 5–7  |
| Alpha Test   | Internal QA + focus group                   | Week 8    |
| Beta Launch  | Public pilot in one state (e.g., AZ or GA)  | Week 10   |
| Full Rollout | Nationwide launch                           | Week 12+  |

---

## Open Questions

- Should we allow candidates to “claim” and verify their profiles?
- How often should candidate data be updated (weekly, live)?
- Do we include ranked-choice voting support in interface?
