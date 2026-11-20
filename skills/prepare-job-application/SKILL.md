---
name: prepare-job-application
description: Coordinate the full job application package from source archive through job analysis, resume review, and cover letter. Also route requests that specify a subset of application materials.
---

# Prepare a job application

Use the [shared workflow](references/workflow.md) to establish the application folder and pass the same target job, folder, source, and application language between stages. If the user invokes this skill without specifying deliverables, prepare the full package: the posting archive and applicable translations, analysis report, resume, and cover letter. For a requested subset, run only the requested stages and any missing dependencies. A single requested stage can also be invoked directly.

## Run the full package

1. Invoke [`analyze-job-posting`](../analyze-job-posting/SKILL.md). Archive the posting before research, then save the analysis report. If the user supplies a usable analysis for this application, preserve it and fill material gaps from available sources.
2. Invoke [`generate-job-resume`](../generate-job-resume/SKILL.md) with that analysis. Show the draft for review and ask what the user wants to change. Apply their edits and wait for explicit approval of the current resume content. Complete the approved resume and its layout checks when compilation is available. If compilation is unavailable, continue from the approved source and disclose the blocker. Pause here until the user has reviewed and approved the resume content.
3. Only after the resume review is complete, invoke [`generate-job-cover-letter`](../generate-job-cover-letter/SKILL.md) with the analysis and approved resume. Show the two options and wait for the user's selection and approval before producing the final letter PDF.

Save and surface each requested deliverable as it is ready. When resuming after user review, continue from the approved inputs already established for this application.

## Run a requested subset

Use `analyze-job-posting` for source capture or analysis. For source capture alone, stop after archiving and delivering the applicable posting text and translations. Use `generate-job-resume` and `generate-job-cover-letter` for the corresponding documents. Resolve dependencies in the order described in the shared workflow. When both the resume and cover letter are requested, complete the resume review checkpoint and pass the approved resume to the letter skill. When the user requests an analysis and drafting, save the analysis and pass the report to the drafting stages.
