# Job Application Skill

[简体中文](README.zh-CN.md)

This Codex skill turns a job posting and your candidate profile into a tailored LaTeX resume and cover letter. It also drafts a concise email when the employer accepts applications by email.

## What to provide

- **A job posting** as a link, pasted text, or attachment. You can also provide an existing job analysis and continue directly to drafting.
- **Your candidate profile.** Copy [profile.template.md](profile.template.md) to a private `profile.md`, fill in the sections that apply to you, and upload it or share its local path with Codex. Add relevant reports, portfolios, or original project or work files if helpful to fill gaps.
- **Optional custom templates.** Provide a resume template, a cover letter template, or both, including any referenced sections, styles, images, or fonts. Each custom template takes precedence over its bundled counterpart.

- **Resume photo (optional).** Supply a photo and confirm you want to use it in the application.

You can drag files into the chat or provide local paths. If sharing a path, keep the original file or a backup. The skill uses private working copies for profile updates and generates application-specific LaTeX files from template copies.

## How to use it

Ask for the original job posting, job analysis file, resume, cover letter, or any combination. If you do not specify which deliverables you want, the skill prepares all four.

1. Invoke `$prepare-job-application` or ask Codex to prepare your application materials. Include the posting or existing analysis. Before your first resume, Codex checks for your profile and relevant supporting materials, then asks about optional templates and a photo if needed. It reuses your private working profile for later applications.
2. Choose a folder for the posting, analysis, and application files, or receive individual downloads. Codex proposes a folder named for the company and role.
3. Review the requested deliverables. If you requested a cover letter, select or combine the two options. Review the translations if the application language differs from your conversation language.
4. Approve the requested resume or selected cover letter for compilation, as applicable. The skill uses a compatible locally installed LaTeX compiler when available and falls back to Codex's built-in LaTeX compiler otherwise. If compilation or export is unavailable, you still receive the `.tex` sources.

Keep completed profiles and application files outside any public repository.

See [Third-Party Notices](THIRD_PARTY_NOTICES.md) for template credits and licenses.
