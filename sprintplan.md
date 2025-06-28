# 🏁 Sprint Plan: CandidateMatch (Windsurf Implementation)

## 🗓️ Overview

**Duration:** 4 Weeks (2 x 2-week sprints)  
**Team:** Product Owner, PM, AI Engineer, Full Stack Dev, UX Designer, Windsurf Agents  
**Tools:** Windsurf, GitHub, Figma, Vercel, PostgreSQL, Supabase, OpenAI API, VoteSmart API

---

## 🎯 Sprint 1: Foundations & MVP Prototype (Weeks 1–2)

### 🎯 Goals:
- Launch onboarding and user survey flow
- Build candidate ingestion pipeline
- Deploy basic matching algorithm
- Create initial UI using Windsurf’s React/Tailwind agents

---

### 🔧 Tasks

#### 🧱 EPIC 1: User Onboarding & Survey
- [ ] Design issue-ranking quiz UX with Windsurf Design Agent
- [ ] Implement onboarding form with Tailwind UI Agent
- [ ] Store preferences in local state or Supabase (anonymous ID)
- [ ] Set up optional stance inputs (sliders or text)

#### 🗂 EPIC 2: Candidate Database (MVP)
- [ ] Define schema for Candidate, Issue, CandidateIssuePosition
- [ ] Build scraping/ETL pipeline via Windsurf Agent (OpenSecrets + BallotReady)
- [ ] Ingest 5 demo candidates across 2 states
- [ ] Apply basic NLP tagging using OpenAI API

#### 🧠 EPIC 3: Match Engine (Prototype)
- [ ] Define scoring logic (weighted cosine similarity)
- [ ] Implement backend function using Windsurf's Python Agent
- [ ] Return sorted candidate matches per user

#### 🧪 EPIC 7: QA & Testing
- [ ] Use Windsurf Test Agent to simulate 5 user scenarios
- [ ] Validate onboarding → match output consistency
- [ ] Accessibility compliance review

---

## ✅ Sprint 1 Deliverables
- Functional onboarding and match flow (static data)
- Visual prototype hosted on Vercel
- Windsurf workflows saved for UI, scoring, data processing

---

## 🚀 Sprint 2: Dynamic Matching, Compare, Action Hub (Weeks 3–4)

### 🎯 Goals:
- Expand candidate data
- Enable detailed match comparisons
- Add voter tools and social sharing
- Finalize full MVP

---

### 🔧 Tasks

#### 🗂 EPIC 2: Candidate Data (Dynamic Expansion)
- [ ] Scale ingestion to 20+ candidates
- [ ] Auto-refresh weekly via agent-scheduled jobs
- [ ] Add citations + confidence score display

#### 🧠 EPIC 3: Match Engine Enhancements
- [ ] Add breakdown view (per issue score)
- [ ] Implement toggle for importance weighting
- [ ] Store match results in database for future use

#### 📊 EPIC 4: Compare & Voter Action
- [ ] Side-by-side candidate comparison view
- [ ] Add voter registration + polling links by ZIP (Vote.org API)
- [ ] Enable match share cards (Windsurf Image Agent)

#### 🔐 EPIC 5: Feedback + Trust Layer
- [ ] Add feedback form for incorrect matches
- [ ] Display source links per candidate stance
- [ ] Log flagged data to admin dashboard

#### 🧪 EPIC 7: QA & Testing (Final Round)
- [ ] Regression test onboarding + match logic
- [ ] Verify responsive des
