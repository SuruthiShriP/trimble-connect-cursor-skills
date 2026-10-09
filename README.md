# trimble-connect-cursor-skills

Shared [Cursor Agent Skills](https://cursor.com/docs) for Trimble Connect engineering.

## Repository layout

Skills follow Cursor’s project layout:

```
.cursor/skills/
└── bug-fix/          # /bug-fix — JIRA → repro → CloudWatch → fix → PR
    ├── SKILL.md
    ├── scripts/
    └── templates/
```

## Using skills in this repo

Open this repository (or add it as a workspace folder) in Cursor. Skills under `.cursor/skills/` are available to the agent in that workspace.

## Using skills globally (optional)

Copy a skill into your user skills directory:

```powershell
xcopy /E /I ".cursor\skills\bug-fix" "%USERPROFILE%\.cursor\skills\bug-fix"
```

Restart Cursor after copying.

## Skills

| Skill | Invoke | Description |
|-------|--------|-------------|
| `bug-fix` | `/bug-fix {jiraUrl} --repo {path} --branch {branch} [--env int]` | End-to-end Connect bug-fix workflow (see `.cursor/skills/bug-fix/SKILL.md`) |
