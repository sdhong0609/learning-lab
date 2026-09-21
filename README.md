<p align="center">
  English | <a href="README.ko.md">한국어</a>
</p>

# Learning Lab

A Codex and Claude Code plugin marketplace for learning code-based skills by building real, working results first.

Included plugins:

- **Learn Like Gabriel Petersson** — Learn programming and AI in this order: real problem → working result → find knowledge gaps → recursive questioning → self-explanation → verification.

> An unofficial project inspired by Gabriel Petersson's publicly shared learning approach. It is not affiliated with or endorsed by Gabriel Petersson.

## Installation

### Codex CLI

Add the marketplace and then install the plugin from your terminal.

```bash
codex plugin marketplace add sdhong0609/learning-lab
codex plugin add learn-like-gabriel-petersson@learning-lab
```

Start a new Codex session after installation to use the plugin.

To install interactively, run `codex`, type `/plugins`, and select `Learn Like Gabriel Petersson` under `Learning Lab`.

### ChatGPT Desktop App

First, add the marketplace from your terminal.

```bash
codex plugin marketplace add sdhong0609/learning-lab
```

Then select `Learning Lab` in the Plugins Directory and install `Learn Like Gabriel Petersson`. Start a new chat after installation.

### Claude Code

Add the marketplace and then install the plugin from your terminal.

```bash
claude plugin marketplace add sdhong0609/learning-lab
claude plugin install learn-like-gabriel-petersson@learning-lab
```

Or, inside a Claude Code session, run `/plugin marketplace add sdhong0609/learning-lab` and then `/plugin install learn-like-gabriel-petersson@learning-lab`.

Start a new Claude Code session after installation. The skill triggers automatically on learning requests, or you can call it directly with `/learn-like-gabriel-petersson:learn-like-gabriel-petersson`.

## Example Prompts

- "I want to learn Python by building a small automation tool."
- "I want to build a working recommendation model first, then understand how it works."
- "I want to learn server development by building a web API myself."

The plugin first builds a minimal working result. It then digs into what you don't know, one piece at a time, and asks you to explain it back so it can check for errors and gaps.

## Structure

```text
learning-lab/
├── .agents/plugins/marketplace.json
├── .claude-plugin/marketplace.json
└── plugins/
    └── learn-like-gabriel-petersson/
        ├── plugin.json
        ├── .codex-plugin/plugin.json
        ├── .claude-plugin/plugin.json
        └── skills/
```

## Status

- Version: `0.1.0`
- Type: Skills-only plugin
- Distribution: GitHub-based marketplace
- Submitted to the official OpenAI Plugins Directory: Not yet
