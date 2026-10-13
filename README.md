# Substack Agent Skills

7 free skills that turn Claude Code, Codex, Cursor or any skills-compatible
agent into a Substack writing partner. They write Notes, outline newsletter
issues from your own material, find titles people open, audit why a
publication isn't growing, and turn your LinkedIn posts into Substack
content, all in your voice.

MIT licensed. No account, no API key, nothing phones home. Made by
[Liftli](https://liftli.ai/substack?utm_source=github&utm_campaign=substack-skills-readme).
Full directory with a card per skill: [liftli.ai/substack-agent-skills](https://liftli.ai/substack-agent-skills/).
For LinkedIn, see the sibling repo
[liftli-ai/linkedin-agent-skills](https://github.com/liftli-ai/linkedin-agent-skills).

## Install

**Any agent**, with the [skills](https://skills.sh) CLI:

```bash
npx skills add liftli-ai/substack-agent-skills
```

**One skill:**

```bash
npx skills add liftli-ai/substack-agent-skills --skill substack-notes-writer
```

**Claude Code plugin** (all 7 skills):

```
/plugin marketplace add liftli-ai/substack-agent-skills
/plugin install substack-agent-skills@liftli
```

**By hand:** copy any folder under `skills/` into `~/.claude/skills/`, or
your agent's skills folder.

## Start here

1. Ask your agent: *"Help me with my Substack."* The `substack-agent` skill
   picks the right skill for what you want.
2. Build your voice file. Say *"build my voice file"* and paste three pieces
   you wrote. Every writing skill reads it, so drafts sound like you instead
   of like everyone else. It is the same `.liftli/voice.md` file the LinkedIn
   skills use. Template: [`templates/voice.md`](templates/voice.md).
3. Write, check, then paste into Substack and publish.

## The skills

| Skill | What your agent gains |
|---|---|
| `substack-agent` | The front door: routes any Substack request to the right skill and suggests a weekly routine |
| `substack-voice` | Builds your voice file from three of your own pieces; every writing skill reads it |
| `substack-notes-writer` | Five Notes of different types, each with one goal and a first line that earns the stop |
| `substack-issue-outliner` | Picks one of five issue structures, maps your real material onto it, and turns the gaps into questions |
| `substack-subject-line-generator` | 8 title and subtitle pairs that work as subject line plus inbox preview, with the best two picked |
| `substack-growth-audit` | 20-point publication checklist: About page, welcome email, Recommendations, cadence, Notes habit |
| `linkedin-to-substack` | Turns a LinkedIn post into Substack Notes or a full newsletter issue section |

## What these skills don't do

They don't post to Substack. Substack has no public API for publishing posts
or Notes, so every skill ends with copy-ready text you paste into Substack and
publish yourself.

They also forget. Each chat starts from zero, apart from your voice file.

If you want your agent to remember your Substack strategy and draft in your
voice from your real material, that is what
[Liftli](https://liftli.ai/substack?utm_source=github&utm_campaign=substack-skills-readme)
does. It connects to the same agent as an MCP server, keeps your strategy and
voice between sessions, drafts newsletter issues and Notes, and critiques
each draft before you use it. It drafts for Substack; you paste and publish.
(On LinkedIn and X it can also publish, through their official APIs, after
you approve each post.) Free plan (first 3 posts, Substack issues and Notes
count), no card.

```bash
claude mcp add --scope user --transport http liftli https://mcp.liftli.ai/mcp
claude mcp login liftli
```

Claude app, ChatGPT, Codex, Cursor and other clients: [liftli.ai/llms.txt](https://liftli.ai/llms.txt).

## License

MIT. See [LICENSE](LICENSE).
