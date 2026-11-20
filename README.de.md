# Codex-Skill für Bewerbungsunterlagen

[English](README.md) · [简体中文](README.zh-CN.md)

Dieser Codex-Skill erstellt anhand einer Stellenausschreibung und deines Bewerbungsprofils einen auf die Stelle zugeschnittenen Lebenslauf und ein Anschreiben in LaTeX. Wenn der Arbeitgeber Bewerbungen per E-Mail annimmt, entwirft er auch eine kurze Bewerbungs-E-Mail.

## Was du bereitstellen solltest

- **Stellenausschreibung.** Sende einen Link zur Ausschreibung, füge den Text ein oder lade die Ausschreibung als Datei hoch. Wenn du bereits eine Stellenanalyse hast, kannst du sie bereitstellen und direkt mit den Entwürfen beginnen.
- **Bewerbungsprofil.** Kopiere die [Profilvorlage](skills/prepare-job-application/profile.template.md) in eine private Datei namens `profile.md`. Fülle die für dich relevanten Abschnitte aus und lade die Datei hoch oder teile Codex den lokalen Pfad mit. Bei Bedarf kannst du Berichte, ein Portfolio oder Originaldateien aus Projekten und früheren Tätigkeiten ergänzen.
- **Eigene LaTeX-Vorlagen (optional).** Du kannst eine eigene Vorlage für den Lebenslauf, das Anschreiben oder beides bereitstellen. Füge auch alle eingebundenen Dateien für Abschnitte, Formatvorlagen, Bilder und Schriften bei. Deine Vorlagen haben Vorrang vor den mitgelieferten Vorlagen.
- **Bewerbungsfoto (optional).** Lade ein Foto hoch und bestätige, dass es für diese Bewerbung verwendet werden darf.

Du kannst Dateien direkt in den Chat ziehen oder ihre lokalen Pfade angeben. Bewahre bei der Angabe eines Pfads die Originaldatei oder eine Sicherungskopie auf. Der Skill aktualisiert das Profil in einer privaten Arbeitskopie und erstellt die LaTeX-Dateien für jede Bewerbung aus Kopien der Vorlagen.

## Installation und Nutzung

Installiere alle vier Ordner unter [`skills/`](skills) nebeneinander im selben Codex-Skill-Verzeichnis. So können die Skills gemeinsame Anweisungen nutzen und fehlende Unterlagen bei Bedarf erstellen. Wenn du eine bestehende Installation von `prepare-job-application` aktualisierst, übernimm die neuen Skill-Dateien in die vorhandene Installation und bewahre dein privates Arbeitsprofil und deine eigenen Vorlagen auf.

| Skill | Einsatzbereich |
| --- | --- |
| [`$prepare-job-application`](skills/prepare-job-application/SKILL.md) | Erstellt standardmäßig die vollständigen Bewerbungsunterlagen oder eine von dir gewählte Auswahl |
| [`$analyze-job-posting`](skills/analyze-job-posting/SKILL.md) | Archiviert und analysiert die Stellenausschreibung oder archiviert sie auf Wunsch ohne Analyse |
| [`$generate-job-resume`](skills/generate-job-resume/SKILL.md) | Erstellt einen auf die Stelle zugeschnittenen Lebenslauf |
| [`$generate-job-cover-letter`](skills/generate-job-cover-letter/SKILL.md) | Erstellt ein auf die Stelle zugeschnittenes Anschreiben |

1. Stelle die Ausschreibung oder eine vorhandene Stellenanalyse bereit. Wähle einen Ordner für die Bewerbung oder den Einzeldownload der Dateien. Bei einem Link speichert Codex die Ausschreibung lokal als PDF oder Offline-Webseite. Anhänge kopiert Codex unverändert, eingefügten Text speichert es als Markdown.
2. Codex speichert einen Analysebericht mit den Anforderungen der Stelle.
3. Prüfe den Lebenslauf und bestätige die überarbeitete Fassung. Wenn du die vollständigen Unterlagen angefordert hast, beginnt Codex mit dem Anschreiben, sobald du den Lebenslauf freigegeben hast.
4. Wähle einen der beiden Anschreibenentwürfe aus oder kombiniere sie und gib die endgültige Fassung frei. Wenn sich die Bewerbungssprache von der Chatsprache unterscheidet, erhältst du zur Prüfung auch eine Übersetzung. Codex verwendet einen kompatiblen lokalen LaTeX-Compiler, sofern verfügbar, und greift andernfalls auf den integrierten Compiler zurück. Falls die Kompilierung oder der Export scheitert, erhältst du die `.tex`-Quelldateien.

Wenn du nur einen Lebenslauf oder nur ein Anschreiben anforderst, sucht Codex im Bewerbungsordner nach der benötigten Stellenanalyse oder dem benötigten Lebenslauf und fragt, ob es die gefundene Datei verwenden darf. Falls die Datei fehlt oder du ihrer Verwendung nicht zustimmst, fragt Codex nach einer vorhandenen Alternative. Ist keine verfügbar, erstellt der entsprechende Skill die fehlende Unterlage.

Bewahre ausgefüllte Profile und Bewerbungsunterlagen außerhalb öffentlicher Repositorys auf.

Informationen zur Urheberschaft und zu den Lizenzen der Vorlagen findest du in den [Lizenzhinweisen zu Drittmaterialien](THIRD_PARTY_NOTICES.md).
