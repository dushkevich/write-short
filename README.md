# write-short

A skill that makes your AI agent write so you understand it on the first read.

It works with Claude Code, Codex, Cursor, Gemini CLI, GitHub Copilot, and any other agent that reads `SKILL.md` skills. For chat apps without skills, there is a short version you can paste.

## Before and after

**Before**
> Great news! I've successfully completed the implementation of the new upload pipeline. Basically, after a thorough investigation, the root cause was rate limiting on the TikTok API side, so I implemented exponential backoff with jitter, which should significantly improve reliability going forward.

**After**
> Uploads to TikTok work again. I ran 5 test uploads, and all 5 went through.
>
> What was wrong: TikTok only lets us upload a few times a minute. When we went over that, it refused, and our code gave up. Now the code waits and tries again.

More examples are in [examples.md](skills/write-short/references/examples.md).

## What's inside

17 rules, in 6 groups, in the order the agent uses them:

- **Before writing:** know the goal, answer first, and say back a decision before acting on it.
- **Words:** cut filler, give facts instead of praise, use plain words, drop jargon and inside names, be exact, say who does what, and call problems by plain names.
- **Sentences and layout:** one new idea per sentence, one topic per block, and the count before a list.
- **Explaining:** start from what the reader knows, and make numbers mean something.
- **Questions:** the situation first, then each option as what will happen, then the agent's pick.
- **Before sending:** reread and edit, with a 10-point checklist.

The full rules are in [SKILL.md](skills/write-short/SKILL.md). Common word swaps are in [plain-words.md](skills/write-short/references/plain-words.md).

## Install

Pick the way that fits your agent.

### Any agent, one command

```bash
npx skills add dushkevich/write-short -g
```

This finds the agents on your computer and adds the skill to each one. `-g` adds it for all your projects. Leave `-g` out to add it to the current project only. You need Node.js 22.20 or later. The command uses the open-source [skills](https://github.com/vercel-labs/skills) installer.

### Claude Code, as a plugin

Run these 2 commands inside Claude Code:

```
/plugin marketplace add dushkevich/write-short
/plugin install write-short@write-short
```

### By hand

Copy the `skills/write-short` folder into your agent's skills folder:

| Agent | For all projects | For one project |
|---|---|---|
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| Codex | `~/.agents/skills/` | `.agents/skills/` |
| Cursor | `~/.cursor/skills/` | `.agents/skills/` |
| Gemini CLI | `~/.gemini/skills/` | `.agents/skills/` |
| GitHub Copilot | `~/.copilot/skills/` | `.agents/skills/` |

For example, for Claude Code:

```bash
git clone https://github.com/dushkevich/write-short.git
cp -r write-short/skills/write-short ~/.claude/skills/
```

### Claude apps

1. Download `write-short.zip` from the [latest release](https://github.com/dushkevich/write-short/releases/latest).
2. In Claude, open **Customize → Skills**, click **+**, and upload the zip.

Skills need code execution, so turn it on in Claude's settings first.

### Chat apps without skills

Paste the text from [RULES-SHORT.md](RULES-SHORT.md) into the app's custom instructions or system prompt. It fits in 1,500 characters, so it works with ChatGPT's custom instructions too.

## Make the agent use it every time

An agent loads a skill only when it decides the skill fits. To make it use this one for every reply, add this line to the file your agent reads at the start of each session:

```
Load the write-short skill before your first message to me, and follow it in every message.
```

That file is `~/.claude/CLAUDE.md` for Claude Code, `~/.codex/AGENTS.md` for Codex, and `~/.gemini/GEMINI.md` for Gemini CLI. Most other agents read `AGENTS.md` in your project.

## License

MIT. See [LICENSE](LICENSE).
