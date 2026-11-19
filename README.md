# Job Application Skill

[简体中文](README.zh-CN.md)

This Codex skill turns a job posting and your candidate profile into a tailored LaTeX resume and cover letter. It also drafts a concise email when the employer accepts applications by email.

## What to provide

- **A job posting** as a link, pasted text, or attachment.
- **Your candidate profile.** Copy [profile.template.md](profile.template.md) to a private `profile.md`, fill in the sections that apply to you, and upload it or share its local path with Codex. Add relevant project notes or other evidence if helpful.
- **Optional custom templates.** Provide a resume template, a cover letter template, or both, including any referenced sections, styles, images, or fonts. Each custom template takes precedence over its bundled counterpart.

## How to use it

1. Invoke `$prepare-job-application` or ask Codex to prepare your application materials. Include the job posting and tell Codex where to find your profile and any custom templates.
2. Review the drafts in the application language. If it differs from your conversation language, review the accompanying translation as well.
3. Approve the drafts for compilation. The skill uses a compatible locally installed LaTeX compiler when available and falls back to Codex's built-in LaTeX compiler otherwise. If compilation or export is unavailable, you still receive the `.tex` sources.

Keep completed profiles and application files outside any public repository.

See [Third-Party Notices](THIRD_PARTY_NOTICES.md) for template credits and licenses.
