# Homepage Workflow: Scholar + Publications Sync + Experience

> Goal: automatically sync papers from Google Scholar into your homepage Publications, support guided replacement from arXiv preprints to officially published versions, and extract Work Experience from your resume into the homepage.
>
> Working style: every step has a confirmation checkpoint. We only move to the next step after your approval.

## Step 0 - Scope Confirmation (No Code Changes)

Input:
- Your Google Scholar profile (already provided)
- Conference/reference source (already provided: https://danais-lab.com/)
- Current homepage repository

Output:
- Final scope checklist:
  - `Publications` (auto sync + manual override)
  - `Work Experience` (from resume)
  - `Google Scholar` section (profile link + metrics)

Confirmation checkpoint:
- Confirm whether we keep everything in `index.md` or move to `_data/*.yml` + rendered sections in `index.md`.

---

## Step 1 - Data Structure Refactor (Foundation First)

Goal: make the homepage data-driven so future updates can be automated.

Implementation:
- Add `_data/publications.yml`
- Add `_data/experience.yml`
- Refactor Publications/Timeline sections in `index.md` to read from `_data`

Recommended fields for publications:
- `id`
- `title`
- `authors`
- `year`
- `venue`
- `status` (`published` / `preprint` / `under_review`)
- `source` (`scholar` / `manual`)
- `scholar_url`
- `arxiv_url`
- `doi_url`
- `pdf_url`
- `code_url`
- `featured` (bool)
- `notes`

Recommended fields for experience:
- `company`
- `role`
- `start`
- `end`
- `location`
- `highlights` (list)
- `logo` (can be empty initially)

Confirmation checkpoint:
- Confirm this field schema. If you want extra fields (for example `impact`, `tech_stack`), we lock them here.

---

## Step 2 - Google Scholar Sync Harness (Automated Ingestion)

Goal: update Scholar publications into local structured data with one command.

Implementation:
- Create `scripts/sync_scholar_publications.py`
- Input Scholar user id (for example `7e89UC8AAAAJ`)
- Output normalized JSON/YAML to `data/generated/scholar_publications.json`
- Dedup strategy: normalized `title + year` (with `arxiv id / doi` as secondary keys)

Sync options (choose one):
1. Lightweight parsing (recommended first): parse Scholar page directly (simpler, moderate stability)
2. Library/API approach: use `scholarly` etc. (stronger model, but dependency/anti-bot risk)

Confirmation checkpoint:
- Confirm which sync option to start with.
- Confirm update mode: full overwrite or incremental merge.

---

## Step 3 - arXiv -> Published Replacement (Semi-Auto + Your Approval)

Goal: replace preprint entries with official venue versions safely.

Implementation:
- Create `data/manual/publication_overrides.yml` (manual override table)
- Fields:
  - `match_key` (recommended: title hash)
  - `replace_venue`
  - `replace_year`
  - `replace_doi_url`
  - `replace_paper_url`
  - `replace_status: published`
  - `evidence_url` (danais-lab / dblp / publisher page)
- Create `scripts/merge_publications.py`
  - Input: Scholar output + overrides
  - Output: `_data/publications.yml`

How danais-lab is used:
- Used as a candidate evidence source to identify papers likely already published.
- Final replacement only happens after your explicit approval via override entries.

Confirmation checkpoint:
- Confirm policy: every arXiv replacement requires your manual approval.

---

## Step 4 - Resume-to-Experience Extraction (Semi-Auto)

Goal: extract work history from `cv/resume.pdf` and map into `_data/experience.yml`.

Implementation:
- Create `scripts/extract_experience_from_resume.py`
- First run writes `data/generated/experience_draft.yml`
- After your review, finalize into `_data/experience.yml`

Image strategy:
- Launch text-first version now (no dependency on logos)
- Later, you add image paths in `logo` (for example `/images/companies/baidu.png`)

Confirmation checkpoint:
- Confirm we go with “text first, images later”.

---

## Step 5 - Homepage Presentation Upgrade (UI Layer)

Goal: present Scholar, Publications, and Experience in a cleaner and maintainable way.

Implementation:
- Keep existing Scholar button in hero section
- Add Scholar summary block:
  - `Total Publications`
  - `Selected Venues`
  - `Last Sync Date`
- Publications list supports:
  - status badges (Published / Preprint)
  - quick links (Paper / arXiv / DOI / Code)
  - descending order by year
- Experience section supports:
  - timeline + company/role cards
  - reserved logo slot

Confirmation checkpoint:
- Confirm style direction: academic-clean vs. portfolio-card-heavy.

---

## Step 6 - One-Command Harness (Daily Use)

Goal: let you run the entire update flow with one command.

Implementation:
- Create `scripts/run_homepage_sync.sh`
- Execution order:
  1. Pull from Scholar
  2. Apply overrides
  3. Generate `_data/publications.yml`
  4. Extract/update experience
  5. Optional local build verification
- Example command:
  - `bash scripts/run_homepage_sync.sh --scholar-id 7e89UC8AAAAJ`

Confirmation checkpoint:
- Confirm CLI options (for example whether to include `--dry-run`).

---

## Step 7 - Human Review and Publish

Goal: keep automation accurate before publish.

Review checklist:
- Any duplicate new papers?
- Any wrong arXiv replacements?
- Author order correct?
- Venue/year aligned with latest records?
- Experience timeline accurate?

Publish action:
- After your approval, I run `git add/commit/push`.

Confirmation checkpoint:
- Confirm whether to auto-generate a Markdown change report before each publish.

---

## Recommended Rollout Order (Most Stable)

1. Complete Step 1 (data structure) + Step 5 (render from data)
2. Then Step 3 (overrides) for controlled correctness
3. Then Step 2/4/6 automation layers

Reason:
- Even if auto-fetch fails temporarily, homepage content remains maintainable via `_data` without blocking updates.

