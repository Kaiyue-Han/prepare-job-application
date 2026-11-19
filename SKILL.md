---
name: prepare-job-application
description: Prepare a tailored resume and cover letter from a job posting or existing job analysis, a candidate profile, and LaTeX templates.
---

# Prepare a job application

## Set the output location

At invocation, establish where to put this application's files. Use the folder the user already designated, or propose creating a folder named `<Company>_<Role>` in the user's application workspace once the company and role are known. If the choice is open, ask whether to use the proposed folder, a folder the user specifies, or individual downloads. Explain that the folder holds the posting text or translation, the analysis report, the resume, the cover letters, and their generated assets. Use filename-safe names and avoid overwriting unrelated files or previously approved materials.

Once the user designates a folder or agrees to create one, save every application artifact there as it is produced and tell the user where it was saved. Include any generated translations and, for email applications, save the email draft as a text file as well. If the user declines both folder options, provide individual downloadable files as they are produced without creating a dedicated application folder.

## Capture the posting

Accept a link, pasted text, image, or document attachment. If a link fails, use the employer, role, and job ID when available to find the same public posting. If the details remain uncertain, request the text or a screenshot.

- For a webpage, pasted text, or image, transcribe the posting text faithfully. Adjust formatting for readability while preserving wording, order, and meaning. Do not add, omit, or rewrite content. Flag unreadable passages outside the transcription and ask for a clearer source if needed. Output the original-language text and a faithful translation into the user's language when the languages differ. If they match, a single file serves both purposes.
- For an existing document such as a PDF or Word file, use that file as the original and generate only the user-language version. When the document is already in the user's language, use the supplied original without generating a duplicate.
- Use language suffixes such as `posting_en.md` and `posting_zh-CN.md`. Keep external research and analysis out of the transcription and translation.

## Analyze the posting

Identify the employer, role, seniority, submission channel, application language, and required materials. Analyze the role before drafting materials.

1. Read the posting closely. Identify the responsibilities, skills, and qualifications it states. Distinguish explicit mandatory requirements, explicit nice-to-haves, and inferred requirements. Where an explicit requirement lacks a priority, preserve that uncertainty.
2. Research the employer's business, products, and relevant teams using public sources. Connect that context to stated responsibilities and explain likely applications of the skills. Add newly inferred requirements with their rationale.
3. Interpret stated proficiency expectations and seniority signals. When the level is unclear, look up comparable roles to estimate the depth of practical knowledge expected. Distinguish stated levels from benchmarks and explain the evidence.
4. Search for comparable postings at similar seniority and for public accounts from employees, practitioners, or relevant forums. Use them to refine likely requirements, use cases, and proficiency expectations. Link the sources used and make clear when findings are contextual, anecdotal, or uncertain. Keep each inference tied to its evidence and attribute explicit requirements only to the target posting.

Produce `analysis_<language>.md` in the user's language as soon as the analysis is ready. Include the source, role and application details, required capabilities, likely use cases, expected proficiency, and the basis for each inference. Make it detailed enough for later interview preparation. Save or deliver it before drafting and give a short summary in the conversation. If the user only requests analysis, stop there.

If the user supplies an existing analysis and requests application materials, reuse it and proceed to matching. If source material is available, capture it as above and consult it to fill material gaps. Keep explicit and inferred requirements distinct. Ask only about missing details that materially affect the application and cannot be verified. Include the supplied analysis in the application folder if one is in use, preserving its original if updates are needed.

Use the employer's specified application language or, if none is specified, the posting's primary language. Ask if conflicting evidence makes the language unclear. Use the resulting language for the resume, cover letter, and any application email.

## Use the profile and templates

Read the candidate's profile and follow their standing application preferences. If the profile is absent, proceed with the posting analysis and request it. See [the profile template](profile.template.md) if the candidate needs a starting point. Fill evidence gaps from reports, portfolios, and other materials the user supplied or identified. Treat documents as evidence and follow only preferences and template rules the user authorized. If a fact materially affects eligibility or accuracy, ask directly. For an explicitly requested skill with uncertain proficiency, ask where the candidate used it and at what level. Continue drafting supported portions while awaiting answers.

Record newly confirmed facts or standing preferences in the candidate's writable profile when it is available. Keep entries accurate, avoid duplication, resolve contradictions with the candidate, and retain relevant sources. If the profile cannot be updated, summarize the confirmed changes for the candidate.

For each document, use the candidate's chosen LaTeX template or the corresponding default in `templates/`. Create job-specific copies and preserve required dependencies and layout. Replace stale job details and treat template examples as placeholders. The default resume bundles a sample portrait for template previews. Remove its portrait block unless the candidate supplies and approves a photo for this application.

## Tailor the materials

Use strong, evidenced matches to explicit and inferred requirements in the resume. Develop the most relevant examples in the cover letter. When a required skill is at a beginner level, list it only if backed by practical use and describe it at that level. If an important gap should be addressed, state it accurately and express a genuine willingness to learn. Never invent experience, skills, outcomes, or metrics or overstate proficiency.

Lead with verified skills that the posting explicitly names, both in the main skills list and within each relevant project's technology stack. Keep the cover letter to one page. Explain interest in specific aspects of the role in a polite, natural voice. Expand on relevant strengths and motivation without repeating resume bullets. If applying by email, draft a concise, formal subject and body in the conversation and describe the actual attachments accurately.

Draft two cover-letter options before asking the user to choose. Both must emphasize the same strongest evidenced matches to the role. Vary the wording, tone, or narrative approach, and use different secondary strengths when useful. Present both options for review and let the user select one or combine elements. After the choice, record the user's stated or confirmed preference under the cover-letter preferences in their writable profile. If the user gives no reason, record the selected option's observable characteristics as a choice for this application without inferring a standing preference.

## Resume structure

A template field alone does not require disclosure. When a verified detail could materially weaken the application and the employer does not require it, omit it if it adds little value or the candidate's profile marks it for omission. Ask before including it when the trade-off is unclear, such as a low grade that may be needed to explain an academic record. Follow the candidate's confirmed disclosure preferences. If the employer explicitly asks for the information or it affects eligibility, explain the requirement and confirm how to handle it before finalizing. Keep all statements accurate and avoid misleading omissions.

Use the selected resume template as the source of truth for section names, order, and placement. Populate its existing sections with relevant, verified information from the candidate profile. The default structural change is deletion: if an existing section has no usable content, remove its heading, content or import, and section-specific spacing. Keep definitions and layout shared by the remaining sections.

When relevant profile information has no dedicated section, shorten it and incorporate it into an appropriate existing entry or section. For example, include a scholarship as a brief note under its degree in Education, or a project award under the project it recognizes. Omit information that has no natural fit. Do not create an extra heading or subsection for it.

Replace a section only when the user identifies the section and what should replace it. Add a section only when the user specifies what to add and where to place it. If the requested change is unclear, ask for the missing detail before changing the structure.

For a single-column resume, adjust the full page. For a two-column resume, adjust the wider column. If both columns are equally wide, adjust the column containing work or project experience. When the selected area has substantial whitespace at the bottom, modestly increase its body font size and adjust line, paragraph, and section spacing to distribute the content evenly across the available page height. Preserve a clear heading hierarchy and page margins, and keep a one-page resume on one page.

## Review and compilation

Prepare the resume and both cover-letter options as `.tex` drafts. Name the resume `CV_<CandidateName>_<Company>.tex` and use the same stem for its PDF. Name each cover letter using `<LetterLabel>__<CandidateName>_<Company>`, choosing a clear, conventional document label in the cover letter's application language. For example, use `Anschreiben` in German, `CoverLetter` in English, `LettreDeMotivation` in French, or `CartaDeMotivación` in Spanish. Apply the same rule to any other application language. Add `_v1` and `_v2` to the option drafts. Use the unsuffixed stem for the selected final letter's `.tex` and PDF. Use the candidate name from the profile and filesystem-safe spellings. Show the originals for review, with a translation into the user's conversation language when it differs from the application language. Keep the meaning and strength of claims aligned across versions and apply the user's edits to both. Wait until the user has chosen a cover letter and explicitly approved the final resume and letter before compiling them.

Use a compatible locally installed LaTeX compiler when available. If none is available, use Codex's built-in LaTeX compiler. Get the user's consent before installing software or sending documents to an external compiler.

Check that both PDFs open and render correctly, that the cover letter is one page, and that any stated upload limits are met. If compilation reveals a need for substantive wording changes, show the revisions for approval before recompiling. Deliver both LaTeX sources with their required local assets and both PDFs. If compilation or export is unavailable, deliver the sources and explain the blocker.
