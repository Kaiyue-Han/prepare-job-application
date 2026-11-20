---
name: generate-job-resume
description: Generate or revise a tailored LaTeX resume (CV) for a specific job. Use for resume-only requests or as the resume step of an application package.
---

# Generate a tailored resume

## Resolve inputs

Set the application folder and resolve the target posting analysis using the [shared workflow](../prepare-job-application/references/workflow.md). Reuse an approved or explicitly supplied analysis, or invoke the analysis skill for the missing input. During a package run, use the analysis already passed by the orchestrator.

## Use the profile and templates

Follow the [candidate profile instructions](../prepare-job-application/references/profile.md) before drafting.

After checking inputs, ask whether the candidate wants to provide a custom resume LaTeX template and a resume photo if their choices are not already recorded. Use the [bundled default](templates/resume.tex) when a custom template is absent. Include a photo only when supplied and approved for use.

For each document, use the candidate's chosen LaTeX template or the corresponding default in `templates/`. Create job-specific copies and preserve required dependencies and layout. Replace stale job details and treat template examples as placeholders. The default resume bundles a sample portrait for template previews. Remove its portrait block unless the candidate supplies and approves a photo for this application.

## Tailor the resume

Use strong, evidenced matches to explicit and inferred requirements in the resume. When a required skill is at a beginner level, list it only if backed by practical use and describe it at that level. If an important gap should be addressed, state it accurately and express a genuine willingness to learn. Never invent experience, skills, outcomes, or metrics or overstate proficiency.

Lead with verified skills that the posting explicitly names, both in the main skills list and within each relevant project's technology stack.

## Resume structure

A template field alone does not require disclosure. When a verified detail could materially weaken the application and the employer does not require it, omit it if it adds little value or the candidate's profile marks it for omission. Ask before including it when the trade-off is unclear, such as a low grade that may be needed to explain an academic record. Follow the candidate's confirmed disclosure preferences. If the employer explicitly asks for the information or it affects eligibility, explain the requirement and confirm how to handle it before finalizing. Keep all statements accurate and avoid misleading omissions.

Use the selected resume template as the source of truth for section names, order, and placement. Populate its existing sections with relevant, verified information from the candidate profile. The default structural change is deletion: if an existing section has no usable content, remove its heading, content or import, and section-specific spacing. Keep definitions and layout shared by the remaining sections.

When relevant profile information has no dedicated section, shorten it and incorporate it into an appropriate existing entry or section. For example, include a scholarship as a brief note under its degree in Education, or a project award under the project it recognizes. Omit information that has no natural fit. Do not create an extra heading or subsection for it.

Replace a section only when the user identifies the section and what should replace it. Add a section only when the user specifies what to add and where to place it. If the requested change is unclear, ask for the missing detail before changing the structure.

For a single-column resume, adjust the full page. For a two-column resume, adjust the wider column. If both columns are equally wide, adjust the column containing work or project experience. When the selected area has substantial whitespace at the bottom, modestly increase its body font size and adjust line, paragraph, and section spacing to distribute the content evenly across the available page height. Preserve a clear heading hierarchy and page margins, and keep a one-page resume on one page.

Apply this layout rule to every generated resume after inserting the actual content; copying template font sizes and spacing is not sufficient. Inspect the effective body font size, line spacing, paragraph or entry gaps, and section gaps in the selected area, including local overrides. Adjust these together as needed so content is distributed as evenly as possible over the usable page height, with consistent spacing between comparable entries and a readable hierarchy. Avoid stretching a single gap to consume the remaining space, crowding text, or adding filler content.

Verify the result after each adjustment. Use reliable rendered-layout calculations if available; source length or a visual guess from LaTeX code alone does not establish even distribution. If the LaTeX source does not allow reliable verification, compile a preview PDF, render its pages, and inspect the entire page for bottom whitespace, uneven gaps, crowded blocks, clipping, and unintended page breaks. Revise font size and spacing and repeat the check until the selected area is visibly balanced and the page-count and readability constraints hold. Recheck after any later content edit. Do not declare the layout complete without this verification; if rendering and reliable calculation are both unavailable, explain the blocker and mark the layout unverified.

## Review and compilation

Name the resume `CV_<CandidateName>_<Company>.tex` and use the same stem for its PDF. Use the candidate name from the profile and filesystem-safe spellings. Follow the [review and compilation instructions](../prepare-job-application/references/review.md).

For a requested resume, show the draft and ask what the user wants to change. Wait for explicit approval of the current content after applying any substantive edits. Make the approved resume source available to the next stage only after this checkpoint when the orchestrator requested a reviewed CV. Check that the resume passes the distribution check above and briefly report the layout verification method and result, including whether font size and spacing were adjusted.

When invoked only to fill a missing cover-letter dependency, save a tailored draft source in the application folder when one is in use and pass its path and verified content back to the caller. Treat this as a supporting draft. Final resume compilation and delivery apply when the user requests the resume itself.
