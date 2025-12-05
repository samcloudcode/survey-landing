# Yacht Survey Reporting App — Overarching Specification (v1 → Scalable Platform)

## Background & Problem

Yacht surveys today are operationally heavy, but the real bottleneck is still **report production**. Surveyors collect complex observations onboard across many systems, then spend days or weeks turning those notes into a polished narrative report. This creates:

* **Long delays** for owners, buyers, brokers, and yards.
* **Inconsistent output quality** depending on time pressure and individual writing style.
* **Liability risk** when wording is speculative, non-standard, or hard to defend.
* **Fragmented evidence** (photos, voice notes, GA markups) that is not cleanly linked to findings.
* **Inspection gaps** when key checks are missed or not logged clearly during long surveys.

There are existing digital survey tools in the market. They do help with **template digitisation, structured capture, and faster form filling**, but the company’s view is that they fall short on the outcomes that matter most:
they **don’t guarantee market-leading narrative quality**, they **don’t remove the write-up bottleneck**, and they **don’t create an evidence-backed, defensible chain of observation**. Their workflows also tend to feel **clunky and “legacy software-y”** in real onboard use.

This product is a deliberate alternative: a **modern, elegant survey capture system paired with a best-in-class report studio**. Using contemporary structured-document frameworks (e.g., rich editors like Tiptap on web) and AI as a co-writer, the app aims to produce **gold-standard reports in hours, with every statement traceable to onboard evidence**—while keeping the workflow lightweight and surveyor-first.

# Goals

## Primary Goals

1. **Market-leading report quality**

   * Produce reports that meet or exceed top-tier professional survey standards.
   * Consistent, neutral, technical language and structure across all reports.

2. **Radical time compression**

   * Convert surveying + reporting into a near-continuous workflow.
   * Reports completed in **hours, not weeks**, with only expert review needed after inspection.

3. **Evidence-backed auditability**

   * Every statement in the report traces to a logged onboard observation.

4. **Surveyor-first workflow**

   * Reduce cognitive load onboard.
   * Make data capture simple, fast, and natural (voice, quick taps, photos).

5. **Scalable beyond internal use**

   * Start as a Cornelsen & Partner productivity engine.
   * Evolve into a subscription platform for the wider yacht survey market.

---

# Unique Selling Propositions (USPs)

1. **Gold-standard output as the core product**

   * Optimized for final report excellence—not just “capturing notes.”

2. **Dictation-centric, AI-assisted surveying**

   * Surveyors speak naturally; AI converts raw observations into polished survey-grade text.

3. **Built-in chain of evidence**

   * Notes, dictations, photos, ratings, and edits auto-log:

     * surveyor identity
     * timestamp
     * geolocation (when available)
     * inspection context (question/category/item)
   * Creates a **defensible audit trail** for every finding.

4. **Reports ready in hours**

   * Drafting happens during capture; post-survey work reduces to review/polish.

5. **Pre-inspection smart question planning**

   * AI generates a tailored, structured inspection plan per vessel and scope.
   * Questions grouped top-level → sub-level, with optimized input types.

6. **Modern portal delivery**

   * Final report plus an evidence portal with links back to photos/notes/voice where appropriate.
   * Distinct views for **surveyor** (full evidence) and **client** (curated evidence).

7. **Multi-deliverable automation**

   * From one dataset, output:

     * full narrative report
     * traffic-light checklist
     * prioritized defect list with cost estimates
     * GA-referenced defect mapping (when GA provided)

**8. Modern report studio as a differentiator**

* The web reporting experience is built on a **structured, modern document framework** (e.g., Tiptap/ProseMirror), enabling:

  * elegant professional layouts,
  * enforced schema consistency,
  * evidence-linked narrative blocks,
  * AI-native rewriting at the right level of structure.
* This is intentionally positioned against legacy “form-to-PDF” tools, raising the ceiling on final report quality and usability.

---

# Competitors & Winning Strategy

## What existing tools are good at today

* **Digitizing templates / structured data capture** onboard.
* **Producing “a report faster”** mainly by form filling.
* Some provide **modern mobile workflows** and decent media handling.

## Why the company views them as insufficient (pain points)

* They **don’t guarantee market-leading narrative quality**; output still depends heavily on after-the-fact writing.
* They **don’t remove the report-writing bottleneck**—they shift it.
* Evidence remains **fragmented or weakly linked** to report statements.
* **Defensibility / liability-safe wording** isn’t built into the generation workflow.
* They tend to feel **clunky and software-heavy** rather than elegant for real onboard use.

## What we must do to outperform decisively — without overcomplication

These are the five “killer advantages” the v1 must deliver elegantly:

1. **Guaranteed gold-standard narrative quality**

   * Structured report schema + AI “polish to standard” per finding/section.
   * AI tone = neutral, technical, liability-safe by design.

2. **Audit trail baked into capture**

   * Every observation logged as a time-stamped, attributed, context-linked event with evidence.
   * Provenance surfaced subtly in the editor (tap to view source).

3. **Hours-to-report workflow**

   * Mobile capture continuously forms a draft report on web.
   * Post-survey dashboard buckets: *Draft ready / Needs review / Missing*.

4. **Evidence-linked portal delivery**

   * Publish yields **report + proof system**.
   * Surveyor vs client permissioned evidence views.

5. **AI pre-inspection question plan**

   * Web generates tailored plan → mobile renders as fast answer cards.
   * Surveyor can answer/skip/add custom inputs; everything logged.

## “Don’t overcomplicate” guardrails for v1

* No heavy template-builder UI yet (just edit/add/reorder).
* No full mobile report editor (capture on mobile, curate on web).
* No regulatory enforcement blocks (assist only).
* No multi-surveyor orchestration UI v1 (event model supports later).
* No offline AI v1 (online transcription/image analysis is fine).

---

# v1 Feature Set

## A. Web App (Prepare + Curate + Deliver)

### 1. Survey Setup & Scoping

* Create survey and define:

  * vessel profile
  * survey type (pre-purchase, warranty, annual, new build, etc.)
  * scope and focus areas
* Upload supporting documents (optional):

  * previous reports
  * certificates
  * General Arrangement (GA) drawings

### 2. AI-Generated Pre-Inspection Question Plan

* AI creates a structured inspection plan:

  * top-level categories
  * sub-sections
  * questions under each sub-section
* Each question includes a **recommended answer mode**:

  * voice note
  * photo/annotation
  * multiple choice
  * numeric field
  * scale/rating
  * free text
* Surveyor can:

  * edit plan
  * add/remove/reorder questions
  * adjust answer types
* Plan is published to mobile.

### 3. Reporting Studio (Tiptap)

* Rich report editor with:

  * structured templates
  * section + finding blocks
  * defect tables
  * inline evidence attachments
* AI tools embedded into editing:

  * rewrite neutrally
  * normalize tone
  * expand dictation into findings
  * summarize findings into section narratives
  * generate defects + priorities + costs
  * generate checklist version

### 4. Survey Dashboard

* Completeness + quality control:

  * planned questions answered
  * skipped/ignored items
  * custom items added onboard
  * evidence coverage
* Flags missing sections, weak evidence, tone inconsistencies.

### 5. Client/Surveyor Portal

* Published report plus evidence-linked portal.
* Permissioned views:

  * **Surveyor:** full notes/audio/metadata/internal evidence.
  * **Client:** curated evidence tied to findings.

---

## B. Mobile App (Onboard Capture Only)

### 1. Load Published Question Plan

* Cached for onboard use.
* Structured navigation by category/subcategory/questions.

### 2. Fast Answer Capture

* For each question:

  * answer via prescribed mode
  * or skip/ignore with one tap
  * or add a custom question/observation
* All actions logged.

### 3. Evidence Capture

* Photos + optional markup
* Voice notes (raw audio)
* Manual specs and ratings
* Optional AI draft preview if online (not required).

### 4. Sync

* Offline capture supported.
* Upload queue for audio/photos; syncs when online.

---

# AI Capabilities (v1)

## 1. Online Speech-to-Text

* Audio recorded on mobile.
* Transcription online after upload.
* Transcript attached to original dictation event.

## 2. Online Image Analysis (optional v1)

* Online processing for:

  * label/text extraction
  * certificate data capture
  * basic image tagging

## 3. AI Drafting + Editing

* Draft findings from transcripts/notes.
* Convert findings into:

  * survey-grade narrative text
  * defect list w/ priorities + costs
  * checklist views
* Liability safeguards:

  * neutral technical tone
  * no speculation wording
  * consistent survey methodology
  * surveyor always final authority

---

# Design Considerations

## 1. Quality-first Reporting

* Enforce:

  * consistent structure
  * consistent technical tone
  * minimal ambiguity
* Web editor must feel like a professional report studio.

## 2. Surveyor Ergonomics

* Onboard UI:

  * one-hand usable
  * low-typing
  * fast, obvious actions
* Default to voice + quick taps.

## 3. Auditability & Evidence Integrity

* Every input includes provenance by default.
* Evidence always linkable to findings.

## 4. Flexibility Without Chaos

* Question plan guides completeness.
* Surveyor can skip/add/override; divergence logged.

## 5. Portal Clarity

* Evidence linking builds trust without overwhelming clients.
* Simple toggles for client visibility.

---

# Architecture Overview

## System Roles

* **Mobile (Flutter):** capture structured inputs + evidence.
* **Web (React + Tiptap):** plan inspection, curate report, deliver portal.
* **Backend (FastAPI):** AI orchestration + trusted knowledge enforcement.
* **Data Layer (Supabase/Postgres):** source of truth for audit events + docs.

## Event-Sourced Data Model (core)

* Every action is an immutable event:

  * question generated/edited
  * question answered/skipped
  * custom question added
  * dictation recorded/transcribed
  * photo captured/annotated
  * report text edited
* Final report is a projection from events + AI synthesis.

## Data Objects

* Survey
* Question Plan (categories → sub-sections → questions)
* Events (action + metadata + provenance)
* Evidence (photos/audio/GA refs)
* Report Document (Tiptap/ProseMirror JSON)
* Exports (PDF/Word/checklist/defect list)

---

# Tech Stack

## Mobile

* **Flutter**

  * iOS + Android single codebase
  * strong offline + media + dictation UX

## Web

* **React / Next.js**
* **Tiptap (ProseMirror)**

  * structured report editor
  * AI-assisted inline editing
  * future collaboration-ready

## Backend

* **FastAPI**

  * AI orchestration endpoints
  * prompt/rules engine
  * STT + image analysis pipelines

## Database / Auth / Storage

* **Supabase**

  * Auth (surveyor + client portal)
  * Storage (photos/audio/GA)
* **Postgres**

  * event log + survey data
  * report documents + projections

---

# v1 Success Criteria

v1 is successful if:

* Surveyor preps on web and inspects onboard with mobile.
* AI question planning improves completeness.
* Dictations/notes generate clean professional findings.
* Audit trail is captured automatically.
* Surveyor finalizes and publishes within hours post-survey.
* Report + portal is client-ready, evidence-linked, and defensible.
