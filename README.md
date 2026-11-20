# Job Application Skill

[简体中文](README.zh-CN.md) · [Deutsch](README.de.md)

This Codex skill turns a job posting and your candidate profile into a tailored LaTeX resume and cover letter. It also drafts a concise email when the employer accepts applications by email.

## What to provide

- **A job posting** as a link, pasted text, or attachment. You can also provide an existing job analysis and continue directly to drafting.
- **Your candidate profile.** Copy [profile.template.md](skills/prepare-job-application/profile.template.md) to a private `profile.md`, fill in the sections that apply to you, and upload it or share its local path with Codex. Add relevant reports, portfolios, or original project or work files if helpful to fill gaps.
- **Optional custom templates.** Provide a resume template, a cover letter template, or both, including any referenced sections, styles, images, or fonts. Each custom template takes precedence over its bundled counterpart.

- **Resume photo (optional).** Supply a photo and confirm you want to use it in the application.

You can drag files into the chat or provide local paths. If sharing a path, keep the original file or a backup. The skill uses private working copies for profile updates and generates application-specific LaTeX files from template copies.

## How to use it

Install all four folders under [`skills/`](skills) as sibling Codex skill directories so they can share instructions and generate missing dependencies. If upgrading an existing `prepare-job-application` installation, merge the updated skill files into it and keep your private working profile and custom templates.

| Skill | Use it for |
| --- | --- |
| [`$prepare-job-application`](skills/prepare-job-application/SKILL.md) | The full package by default, or a specified subset |
| [`$analyze-job-posting`](skills/analyze-job-posting/SKILL.md) | The posting archive and job analysis, or just the archive if requested |
| [`$generate-job-resume`](skills/generate-job-resume/SKILL.md) | A tailored resume |
| [`$generate-job-cover-letter`](skills/generate-job-cover-letter/SKILL.md) | A tailored cover letter |

1. Provide the posting or an existing analysis and choose an application folder or individual downloads. For a posting link, Codex saves a local PDF or offline webpage. It copies an attachment as supplied and saves pasted text as Markdown.
2. Codex saves the analysis report with the requirements for applicants.
3. Review the tailored resume and confirm any edits. Codex starts the cover letter after you approve the resume for a full package.
4. Select or combine the two cover-letter options and approve the final text. Review drafts include a translation when the application language differs from your conversation language. Codex uses a compatible local LaTeX compiler when available and falls back to the built-in compiler. If compilation or export is unavailable, you still receive the `.tex` sources.

For a resume-only or cover-letter-only request, Codex checks the application folder for dependencies and asks permission to use files it finds. If you decline or a file is missing, it asks for an existing alternative before generating the missing dependency with the corresponding skill.

Keep completed profiles and application files outside any public repository.

See [Third-Party Notices](THIRD_PARTY_NOTICES.md) for template credits and licenses.
