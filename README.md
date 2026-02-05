# Claude Skills

Custom skills collection for [Claude Code](https://claude.com/product/claude-code).

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## Skills

| Skill | Description |
|-------|-------------|
| [building-wireframes](./building-wireframes) | Generate lo-fi wireframes as single HTML files with Tailwind CSS |
| [restarting-server](./restarting-server) | Restart Node.js dev server with cache cleanup |

## Installation

### Global (all projects)

```cmd
git clone https://github.com/baslie/claude-skills.git %TEMP%\claude-skills
xcopy /E /I %TEMP%\claude-skills\<skill-name> %USERPROFILE%\.claude\skills\<skill-name>
rmdir /S /Q %TEMP%\claude-skills
```

### Local (current project)

```cmd
git clone https://github.com/baslie/claude-skills.git %TEMP%\claude-skills
xcopy /E /I %TEMP%\claude-skills\<skill-name> .claude\skills\<skill-name>
rmdir /S /Q %TEMP%\claude-skills
```

Replace `<skill-name>` with the skill you want to install.

## Usage

After installation, invoke skills in Claude Code:

- `/building-wireframes` — create a wireframe
- `/restarting-server` — restart dev server

Or describe what you need:

> "Create a wireframe for a SaaS landing page"
> "Restart the server and clear cache"

## Skill Structure

```
skill-name/
├── SKILL.md           # Skill definition
├── assets/            # Templates, images
└── references/        # Additional documentation
```

## License

[MIT](LICENSE)
