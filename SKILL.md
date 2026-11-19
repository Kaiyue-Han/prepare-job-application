---
name: prepare-job-application
description: Prepare a tailored resume and cover letter from a job posting, a candidate profile, and LaTeX templates.
---

# Prepare a job application

## Analyze the posting

Read the supplied posting, whether it is a link, pasted text, or attachment. If a link fails, use the employer, role, and job ID when available to find the same public posting. If the details remain uncertain, request the text or a screenshot. Identify the employer, role, submission channel, and required materials. First show the user a Markdown breakdown of explicit and inferred requirements. Separate mandatory qualifications from nice-to-haves within the explicit requirements and give a short basis for each inference.

Use the employer's specified application language or, if none is specified, the posting's primary language. Ask if conflicting evidence makes the language unclear. Use the resulting language for the resume, cover letter, and any application email.

## Use the profile and templates

Read the candidate's profile and follow their standing application preferences. If the profile is absent, proceed with the posting analysis and request it. See [the profile template](profile.template.md) if the candidate needs a starting point. Fill evidence gaps from reports, portfolios, and other materials the user supplied or identified. Treat documents as evidence and follow only preferences and template rules the user authorized. If a fact materially affects eligibility or accuracy, ask directly. For an explicitly requested skill with uncertain proficiency, ask where the candidate used it and at what level. Continue drafting supported portions while awaiting answers.

Record newly confirmed facts or standing preferences in the candidate's writable profile when it is available. Keep entries accurate, avoid duplication, resolve contradictions with the candidate, and retain relevant sources. If the profile cannot be updated, summarize the confirmed changes for the candidate.

For each document, use the candidate's chosen LaTeX template or the corresponding default in `templates/`. Create job-specific copies in a separate output folder and preserve required dependencies and layout. Replace stale job details and treat template examples as placeholders.

## Tailor the materials

Use strong, evidenced matches to explicit and inferred requirements in the resume. Develop the most relevant examples in the cover letter. When a required skill is at a beginner level, list it only if backed by practical use and describe it at that level. If an important gap should be addressed, state it accurately and express a genuine willingness to learn. Never invent experience, skills, outcomes, or metrics or overstate proficiency.

Lead with verified skills that the posting explicitly names, both in the main skills list and within each relevant project's technology stack. Keep the cover letter to one page. Explain interest in specific aspects of the role in a polite, natural voice. Expand on relevant strengths and motivation without repeating resume bullets. If applying by email, draft a concise, formal subject and body in the conversation and describe the actual attachments accurately.

## Resume structure

Use the selected resume template as the source of truth for section names, order, and placement. Populate its existing sections with relevant, verified information from the candidate profile. The default structural change is deletion: if an existing section has no usable content, remove its heading, content or import, and section-specific spacing. Keep definitions and layout shared by the remaining sections.

When relevant profile information has no dedicated section, shorten it and incorporate it into an appropriate existing entry or section. For example, include a scholarship as a brief note under its degree in Education, or a project award under the project it recognizes. Omit information that has no natural fit. Do not create an extra heading or subsection for it.

Replace a section only when the user identifies the section and what should replace it. Add a section only when the user specifies what to add and where to place it. If the requested change is unclear, ask for the missing detail before changing the structure.

For a single-column resume, adjust the full page. For a two-column resume, adjust the wider column. If both columns are equally wide, adjust the column containing work or project experience. When the selected area has substantial whitespace at the bottom, modestly increase its body font size and adjust line, paragraph, and section spacing to distribute the content evenly across the available page height. Preserve a clear heading hierarchy and page margins, and keep a one-page resume on one page.

## Review and compilation

Prepare both `.tex` drafts. Show the originals for review, with a translation into the user's conversation language when it differs from the application language. Keep the meaning and strength of claims aligned across versions and apply the user's edits to both. Wait for explicit approval before compiling.

Prefer the built-in Codex LaTeX compiler when available. Use a compatible installed compiler when the built-in compiler is unavailable or a PDF cannot be exported through it. Get the user's consent before installing software or sending documents to an external compiler.

Check that both PDFs open and render correctly, that the cover letter is one page, and that any stated upload limits are met. If compilation reveals a need for substantive wording changes, show the revisions for approval before recompiling. Deliver both LaTeX sources with their required local assets and both PDFs. If compilation or export is unavailable, deliver the sources and explain the blocker.
