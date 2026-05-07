# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Language

永远使用中文进行交流、回答和代码注释。所有输出内容都使用中文。

## Purpose

This is a personal Claude Code configuration backup repository. It stores reusable agent skills and safe project-level settings. Sensitive files (API keys, session data, telemetry) are excluded via `.gitignore`.

## Custom skills

- **find-skills** (`.agents/skills/find-skills/SKILL.md`): Helps users discover and install agent skills from the open ecosystem. Searches the [skills.sh](https://skills.sh/) leaderboard and runs `npx skills find <query>` for targeted lookups. Always verify install count, source reputation, and GitHub stars before recommending a skill.

## Network

GitHub access uses SSH over `ssh.github.com` rather than direct `github.com` DNS resolution. The `~/.ssh/config` routes traffic transparently:

```
Host github.com
    Hostname ssh.github.com
    User git
    IdentityFile ~/.ssh/id_ed25519
```

When invoking `gh` CLI or downloading from github.com, you may need to use `ssh.github.com` as the resolved host.
