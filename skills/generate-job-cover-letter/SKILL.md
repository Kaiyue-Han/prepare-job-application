---
name: generate-job-cover-letter
description: Generate or revise a tailored LaTeX cover letter or motivation letter for a specific job. Use for letter-only requests or as the final drafting step of an application package.
---

# Generate a tailored cover letter

## Resolve inputs

Set the application folder and use the [shared workflow](../prepare-job-application/references/workflow.md) to resolve the target posting analysis and a suitable resume. For a package run, use the supplied analysis and the resume already reviewed in that run. For a letter-only request, obtain confirmation before using any matching file discovered in the project folder. If a dependency must be generated, invoke the corresponding skill and pass the resolved inputs to it. Finish resolving both inputs before drafting.

## Use the profile and template

Follow the [candidate profile instructions](../prepare-job-application/references/profile.md) before drafting.

After checking inputs, ask whether the candidate wants to provide a custom cover-letter LaTeX template if their choice is not already recorded. Use the [bundled default](templates/letter.tex) when a custom template is absent.

For each document, use the candidate's chosen LaTeX template or the bundled default. Create job-specific copies and preserve required dependencies and layout. Replace stale job details and treat template examples as placeholders.

## Tailor the cover letter

Select at most one or two strongly relevant experiences or concrete examples in total to substantiate the candidate's strengths and their fit with specific role requirements. Exclude weakly related projects. Organize the argument around capabilities and contribution, not a project-by-project account of tasks performed. When a required skill is at a beginner level, list it only if backed by practical use and describe it at that level. If an important gap should be addressed, state it accurately and express a genuine willingness to learn. Never invent experience, skills, outcomes, or metrics or overstate proficiency.

Before drafting any cover letter, read [Writing a cover letter](references/cover-letter.md). Apply it in the application language, including for letter-only requests. Reuse relevant information from any supplied resume, profile, and posting analysis. If applying by email, draft a concise, formal subject and body in the conversation and describe the actual attachments accurately.

Draft two cover-letter options before asking the user to choose. Both must emphasize the same strongest evidenced matches to the role. Vary the wording, tone, or narrative approach, and use different secondary strengths when useful. Present both options for review and let the user select one or combine elements. After the choice, record the user's stated or confirmed preference under the cover-letter preferences in their writable profile. If the user gives no reason, record the selected option's observable characteristics as a choice for this application without inferring a standing preference.

Save the application email draft as text in the application folder if one is in use.

## Review and compilation

Prepare both cover-letter options as `.tex` drafts. Name each cover letter using `<LetterLabel>__<CandidateName>_<Company>`, choosing a clear, conventional document label in the cover letter's application language. For example, use `Anschreiben` in German, `CoverLetter` in English, `LettreDeMotivation` in French, or `CartaDeMotivación` in Spanish. Apply the same rule to any other application language. Add `_v1` and `_v2` to the option drafts. Use the unsuffixed stem for the selected final letter's `.tex` and PDF. Use the candidate name from the profile and filesystem-safe spellings. Follow the [review and compilation instructions](../prepare-job-application/references/review.md). Wait for the user to select or combine the options and explicitly approve the final content before producing the final approved PDF. Check that the letter meets its length requirement.
