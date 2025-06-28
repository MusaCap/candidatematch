# 🗃️ CandidateMatch Data Model

This document outlines the core entities and relationships in the CandidateMatch application.

---

## 📌 Entity: User

| Field           | Type        | Description                                  |
|----------------|-------------|----------------------------------------------|
| user_id        | UUID        | Unique identifier for the user               |
| email          | String      | Optional, used for account linking           |
| created_at     | Timestamp   | Account creation time                        |
| voter_profile  | JSON        | Contains issue rankings and values stance    |
| location       | String      | ZIP code or district for candidate filtering |
| is_anonymous   | Boolean     | True if user is not logged in                |

---

## 📌 Entity: Issue

| Field        | Type      | Description                                   |
|-------------|-----------|-----------------------------------------------|
| issue_id    | UUID      | Unique ID for the issue                       |
| name        | String    | Name of the issue (e.g., Healthcare)          |
| category    | String    | Grouping (e.g., Economy, Social)              |
| description | Text      | Explainer content for users                   |
| keywords    | [String]  | Keywords used to extract stances via NLP      |

---

## 📌 Entity: UserIssuePreference

| Field         | Type      | Description                                     |
|--------------|-----------|-------------------------------------------------|
| user_id      | UUID      | Links to User                                  |
| issue_id     | UUID      | Links to Issue                                 |
| importance   | Integer   | User-rated importance (e.g., 1–5 scale)         |
| user_stance  | Text      | Optional input (slider, text) on the issue      |

---

## 📌 Entity: Candidate

| Field           | Type      | Description                                  |
|----------------|-----------|----------------------------------------------|
| candidate_id    | UUID      | Unique candidate ID                          |
| name            | String    | Full name                                    |
| office          | String    | Position running for                         |
| party           | String    | Political party                              |
| state           | String    | State or region                              |
| district        | String    | Congressional district (if applicable)       |
| photo_url       | String    | Profile photo                                |
| bio             | Text      | Short biography                              |
| website         | String    | Campaign website                             |
| verified        | Boolean   | Candidate-claimed profile                    |

---

## 📌 Entity: CandidateIssuePosition

| Field            | Type     | Description                                              |
|------------------|----------|----------------------------------------------------------|
| candidate_id     | UUID     | Links to Candidate                                       |
| issue_id         | UUID     | Links to Issue                                           |
| stance_summary   | Text     | NLP-generated summary of position                        |
| confidence_score | Float    | System-assigned confidence (0–1 scale)                   |
| position_vector  | [Float]  | Embedding vector for matching algorithm                  |
| sources          | [String] | URLs or citations supporting stance                      |

---

## 📌 Entity: MatchResult

| Field           | Type     | Description                                            |
|-----------------|----------|--------------------------------------------------------|
| match_id        | UUID     | Unique match record                                   |
| user_id         | UUID     | Links to User                                         |
| candidate_id    | UUID     | Links to Candidate                                    |
| match_score     | Float    | Total weighted alignment score (0–1 scale)            |
| breakdown       | JSON     | Per-issue match analysis (issue_id → score)           |
| generated_at    | Timestamp| Time of match computation                             |

---

## 📌 Entity: Feedback

| Field          | Type      | Description                                          |
|----------------|-----------|------------------------------------------------------|
| feedback_id    | UUID      | Unique feedback entry                               |
| user_id        | UUID      | (Optional) Who gave the feedback                    |
| type           | String    | 'data_error', 'suggestion', 'match_disagreement'    |
| reference_id   | UUID      | Can reference match_id or candidate_id              |
| comments       | Text      | Freeform user notes                                 |
| submitted_at   | Timestamp | When feedback was submitted                         |

---

## 🔗 Relationships

- **User** ↔ **UserIssuePreference**: One-to-many
- **User** ↔ **MatchResult**: One-to-many
- **Candidate** ↔ **CandidateIssuePosition**: One-to-many
- **User** ↔ **Feedback**: Optional one-to-many
- **Issue** links to both **UserIssuePreference** and **CandidateIssuePosition**

---

## 🧠 Notes on NLP Matching Engine

- Candidate statements are embedded into a vector space.
- User preferences are translated into topic vectors based on keyword mapping and stance.
- Match score = weighted similarity across all priority issues (dot product or cosine similarity).

---

## 🔐 Security & Privacy

- Personally Identifiable Information (PII) is hashed or encrypted at rest.
- Match results are stored anonymously unless user creates an account.
- Audit logs track changes to candidate data and NLP models.

