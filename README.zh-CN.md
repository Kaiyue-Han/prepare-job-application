# 求职申请材料 Skill

[English](README.md) · [Deutsch](README.de.md)

这个 Codex Skill 根据岗位描述和个人档案生成有针对性的 LaTeX 简历与动机信。需要通过邮箱申请时，它也会起草简短正式的邮件。

## 需要提供什么

- **岗位描述。** 提供招聘网页链接、岗位正文或附件。也可以提供已有的岗位分析，直接进入材料起草环节。
- **个人档案。** 将 [英文档案模板](skills/prepare-job-application/profile.template.md) 复制为私下保存的 `profile.md`，填写适用的部分，再上传文件或告诉 Codex 本地路径。如需补充经历，也可以提供相关报告、作品集、原项目文件或工作资料。
- **自定义 LaTeX 模板（可选）。** 可替换简历或动机信模板，或两份都换。请一并提供模板引用的章节文件、样式、图片或字体。未指定的部分使用内置模板。

- **简历照片（可选）。** 提供照片并确认希望用于申请。

文件可以直接拖到对话框，也可以提供本地路径。通过路径提供时，建议保留原件或备份。Skill 会在私有工作副本里更新个人档案，并从模板副本生成每次申请的 LaTeX 文件。

## 如何使用

把 [`skills/`](skills) 下的四个目录安装到同一个 Codex 技能目录，以便它们共享规则并生成缺失的依赖。升级旧版 `prepare-job-application` 时，将新版文件合并到已有目录，并保留私有个人档案和自定义模板。

| Skill | 用途 |
| --- | --- |
| [`$prepare-job-application`](skills/prepare-job-application/SKILL.md) | 默认生成全套申请材料，也接受指定组合 |
| [`$analyze-job-posting`](skills/analyze-job-posting/SKILL.md) | 归档岗位并生成分析报告，也可只归档 |
| [`$generate-job-resume`](skills/generate-job-resume/SKILL.md) | 生成针对该岗位的简历 |
| [`$generate-job-cover-letter`](skills/generate-job-cover-letter/SKILL.md) | 生成针对该岗位的动机信 |

1. 提供岗位信息或已有分析，并选择申请文件夹或逐个下载。网页保存为本地 PDF 或离线网页，附件按原样复制，粘贴的正文排版后保存为 Markdown。
2. Codex 保存分析报告，在报告中写明岗位对申请者的要求。
3. 核对简历并确认修改。生成全套材料时，Codex 等你确认简历内容后才开始写动机信。
4. 从两版动机信中选择一版或合并，再确认最终内容。申请语言与对话语言不同时，审阅稿会提供译文。优先使用本机兼容的 LaTeX 编译器，其次使用 Codex 内置编译器；如果无法编译或导出，仍会交付 `.tex` 源文件。

只请求简历或动机信时，Codex 会先在申请文件夹查找所需分析或简历，并询问能否使用找到的文件。文件缺失或你拒绝使用时，Codex 会先询问是否有其他现成文件，再调用对应技能补齐缺失的依赖。

请在公开仓库之外保存填写后的个人档案和申请材料。内置模板的作者、来源和许可证见[第三方许可说明](THIRD_PARTY_NOTICES.md)。
