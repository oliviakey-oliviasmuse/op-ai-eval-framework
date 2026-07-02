# Other Agent Tools

This framework is a Mavis skill, but the content works with any AI agent that accepts instruction files or system prompts.

## Claude Code

Reference the skill directory directly in your project:

```bash
# Add to your project's .claude/
mkdir -p .claude/commands
# Copy SKILL.md into your project as CLAUDE.md
cp skills/op-ai-eval/SKILL.md CLAUDE.md
```

Or reference individual agents:
```
# In a Claude Code session
@agents/eval-coordinator.md
@agents/scenario-designer.md
```

## Cursor

Copy any `SKILL.md` into `.cursor/rules/`, or reference the full `skills/` directory.

## Gemini CLI

```bash
gemini skills install ./op-ai-agent-eval-framework/skills/ --path skills
```

## Windsurf

Add skill contents to your Windsurf rules configuration.

## Generic agent instructions

Skills are plain Markdown. Any agent that accepts instruction files or system prompts can use them. Copy the `SKILL.md` content into your agent's system prompt or reference the relevant sections.

## Quick reference

| Tool | How to use |
|---|---|
| Mavis | `skill: op-ai-eval-framework` |
| Claude Code | Copy SKILL.md as CLAUDE.md |
| Cursor | Copy to `.cursor/rules/` |
| Gemini CLI | `gemini skills install ./skills/` |
| Windsurf | Add to rules configuration |
| Generic | Copy SKILL.md to system prompt |

