---
name: analyze-job-posting
description: Archive a job posting and produce a source-backed job analysis report. Use for posting-only capture, analysis-only requests, or the analysis stage of an application package.
---

# Analyze a job posting

## Request the candidate profile first

At the start of any analysis request, including when this skill is called as a dependency, check whether the user has already supplied a candidate profile file or explicitly provided a local path to it for this application. If so, use it. Otherwise, ask the user to upload the profile file or provide its local path. Wait for a usable profile or an explicit decision to proceed without one before starting analysis. An unanswered request leaves analysis pending. If the user declines to provide a profile, proceed with the role analysis and omit new candidate-specific assessment.

For posting-only capture, proceed with the archive directly. For analysis requests, the posting may be archived after asking for the profile while the reply is pending.

Use the [shared workflow](../prepare-job-application/references/workflow.md) to establish the application folder. If the caller already archived the same source during this run, use that archive. For a posting-only request, stop after capture. When the user supplies a report to reuse, follow [Reuse an existing analysis](#reuse-an-existing-analysis) after capturing any provided posting.

## Capture the posting

Accept a link, pasted text, image, or document attachment. If a link fails, use the employer, role, and job ID when available to find the same public posting. If the details remain uncertain, request the text or a screenshot.

Archive the source locally as soon as the posting is readable, before research or drafting. Use the application folder when one is in use. If the user chose individual downloads, use a writable staging location and make requested archives available as downloads.

- **Webpage:** Save the rendered posting as a PDF or a readable offline webpage with the resources it needs. Verify that the local copy opens and contains the actual posting, including any content revealed by expanding sections. Retain the source URL and capture date alongside the archive. If a method yields a login page, empty shell, or incomplete content, try the other archival format. If the posting still cannot be archived, request a readable copy and save that as the source.
- **Attachment or local file:** Save an unchanged copy in the application folder, including for screenshots or images. Use the existing file when it is already in the folder.
- **Pasted text:** Save the original text as a formatted Markdown file. Preserve its wording, order, and meaning. Use this file as both the archive and the original-language transcription.

Preserve the original-language text and provide a faithful translation as applicable.

- For a webpage, pasted text, or image, transcribe the posting text faithfully. Adjust formatting for readability while preserving wording, order, and meaning. Do not add, omit, or rewrite content. Flag unreadable passages outside the transcription and ask for a clearer source if needed. Output the original-language text and a faithful translation into the user's language when the languages differ. If they match, a single file serves both purposes.
- For an existing document such as a PDF or Word file, use that file as the original and generate only the user-language version. When the document is already in the user's language, use the supplied original without generating a duplicate.
- Use language suffixes such as `posting_en.md` and `posting_zh-CN.md`. Keep external research and analysis out of the transcription and translation.

If the original posting is requested, deliver the local archive and any applicable transcription and translation. For supporting capture, save the files locally so later stages can reopen them.

## Analyze the posting

Identify the employer, role, seniority, submission channel, application language, and required materials. Analyze the role before drafting materials.

1. **Read the target posting closely.** Extract the responsibilities, eligibility criteria, skills, described work, and collaborators. Distinguish mandatory requirements, preferences, nice-to-haves, illustrative tools, and stated requirements of unspecified priority. Preserve original wording when it affects the interpretation.
2. **Research the employer and team.** Use public sources to understand the employer's business, products, the department that owns the role, and related teams. Establish what the team does, which parts of the business or users it serves, and how the stated responsibilities fit into that work. Record verified findings and their sources.
3. **Search the web for job postings at comparable levels.** Prioritize postings with similar work and seniority. Record their stated capabilities, tools, and expected depth of practical experience. Explain the similarities and material differences, then use the postings to benchmark typical requirements and proficiency at that level.
4. **Search the web for first-hand accounts from employees and practitioners in comparable roles and industries.** Run this search separately. Look first for the closest matches, such as current or former employees in the target team or role at the target level. If those are scarce, keep seniority comparable and look for similar roles, similar day-to-day work, or a similar industry background. Prefer the accounts with the strongest overlap with the target duties. Expand to different seniority levels only when comparable-level accounts leave a material gap. Within each tier, start with first-person employee accounts on forums, employee-review sites, or practitioner communities. Prefer accounts with enough concrete detail to assess the work and seniority. Use industry interviews or talks as a secondary source when direct accounts are sparse or need corroboration. Read the original accounts, record what people did, which methods or technologies they used, and the scope of their responsibility. Link the accounts and note the limits of individual or anonymous reports. State when sufficiently comparable detail is unavailable.
5. **Reason from the target role's own information.** Use the department, the posting's specific applicant requirements, and its description of the work to infer likely tasks, work scenarios, and capabilities. Show which known facts jointly support each conclusion and how they connect. Cross-check against employer and team research, comparable postings, and employee accounts. Explain where those sources support, refine, or limit the inference. Attribute explicit requirements only to the target posting.

## Write the analysis report

Produce `analysis_<language>.md` in the user's requested language, defaulting to the conversation language. For Simplified Chinese, use `analysis_zh-CN.md` and write the report in idiomatic Simplified Chinese. Use the employer's specified application language for the resume, cover letter, and any application email, or the posting's primary language if none is specified. Ask if conflicting evidence makes the application language unclear.

### Role and application details

State the role's purpose, main responsibilities, and department. Record eligibility, start date, application channel, required documents, and deadlines where stated. Use the archived posting and the actual application form when accessible. If they differ, attribute each statement to its source and distinguish an upload prompt from a field marked required.

### Explicit requirements

Use the target posting to distinguish eligibility, mandatory requirements, preferences, nice-to-haves, illustrative tools, and requirements of unspecified priority. Include the original wording when it affects eligibility, priority, or required proficiency, alongside the explanation in the report's language.

### Research findings and sources

Present the findings before the inferences and link sources next to the claims they support. Describe gaps where a source category lacks relevant detail.

- **Employer and team.** Present relevant findings about the business, products, department responsibilities, related teams, and working relationships.
- **Comparable job postings.** Show the roles, levels, responsibilities, and stated requirements. Explain what makes each posting comparable and which differences affect the comparison.
- **Employee, practitioner, and forum accounts.** Present the closest matches first. For each account, identify the source type and the person's role or seniority when known, describe the specific work they reported, and explain what makes it comparable to the target role. Flag differences in seniority, responsibilities, or industry and explain how they limit the inference. If using a different-level account, state what gap in comparable-level evidence it helps address.

### Inferred capabilities and work scenarios

For each material inference, show the evidence, the reasoning from that evidence to the conclusion, and what remains uncertain. Consider the target posting's requirements and description of the work, employer and team research, comparable postings, and employee accounts. Cite the sources that actually inform the conclusion. Explain conflicting signals or material gaps, and leave unsupported conclusions open.

1. **Proficiency.** Explain what a person at this level should be able to do in each core capability. Use concrete examples such as explaining the principles, completing a task with guidance, handling routine work independently, or taking responsibility for design and optimization. Distinguish the level stated by the employer from benchmarks in comparable postings and practical clues from employee accounts.
2. **Specific capabilities and technical details.** Infer which parts of a technology the work might require, what problems they would solve, and how deeply the candidate may need to know them. For example, if the posting mentions SQL and processing data from multiple sources, use the duties and research to assess whether joins, data cleaning, validation, or query optimization are likely to matter. Give the basis for each relevant judgment.
3. **Likely work scenarios.** Describe what tasks might arise in the department, who the employee may work with, what steps the work could involve, what they might deliver, and why the capabilities matter in those situations. Identify which scenarios follow from information about the target role and which draw on comparable postings or employee accounts.
4. **Other supported inferences.** Include other findings that materially affect how to understand the role, such as ways of working with other teams, likely priorities, delivery standards, or the boundaries of responsibility. State the conditions and uncertainty behind these conclusions.

### Role technology stack

Summarize the relevant languages, frameworks, databases, platforms, analytics tools, and collaboration tools in a dedicated subsection. For each item, state whether it is explicitly required, preferred or a nice-to-have, an example in the posting, or an inference from research. Briefly describe its likely use. For technologies identified in other postings or employee accounts, cite the source and explain the connection to the target role.

### Candidate fit and preparation

If relevant candidate evidence is available, describe fit, gaps, and preparation suggestions separately after the role analysis. Make the report detailed enough for interview preparation and usable without a candidate profile.

Prioritize coverage of every substantive posting requirement, application detail that affects the candidate, and supported research finding or inference. Combine closely related points where useful while preserving distinctions that change the interpretation. Identify unresolved points when evidence is insufficient.

Save the report before drafting any application documents. If the user only requests analysis, deliver the report file and stop there.

## Reuse an existing analysis

Preserve the original analysis in the application folder if one is in use. Consult any available posting to fill material gaps and keep explicit requirements and inferences distinct. Save changes separately if the original needs updating. Ask only about missing details that materially affect the application and cannot be verified. When analysis is a requested deliverable, save and deliver the usable report before handoff.

For either route, pass the report path, archive path if available, and application language to the calling skill.
