# ND Contract Request skill

An [Agent Skill](https://agentskills.io) that walks a University of Notre Dame requester through preparing a BuyND+ contract request. The assistant:

1. Collects the contract and related documents (files, pasted text, or URLs).
2. Runs a **completeness review**: finds every policy, addendum, DPA, exhibit, or other document the contract references, and flags the missing ones.
3. Produces a plain-language summary, business terms, and potential concerns (indemnity, governing law, data privacy, auto-renewal, and so on).
4. Interviews the requester only for the BuyND+ answers the documents can't supply, following the form's conditional logic.
5. Delivers a report with copy-ready BuyND+ answers to attach to the request.

It is a port of the ND Contract Request Assistant web app and works with any assistant that supports the Agent Skills format. It needs no API keys, servers, or scripts.

## Contents

```
nd-contract-request/
├── SKILL.md                         # Workflow the assistant follows
├── references/buynd-form-fields.md  # BuyND+ questions, conditional logic, departments
└── assets/report-template.md        # Final report layout
```

## Install

The folder name must stay `nd-contract-request` (it matches `name` in `SKILL.md`).

- **Claude Code**: copy the folder to `~/.claude/skills/` (personal) or `.claude/skills/` in a project.
- **Claude.ai / Claude Desktop**: zip the folder and upload it under Settings → Capabilities → Skills.
- **Other skill-aware agents** (OpenAI Codex, Gemini CLI, Cursor, GitHub Copilot, etc.): copy the folder into that tool's skills directory. Check the tool's docs for the current location.
- **Chat apps without skill support** (a Custom GPT, a Gemini Gem, a Copilot agent): paste the body of `SKILL.md` into the instructions and upload `references/buynd-form-fields.md` and `assets/report-template.md` as knowledge files.

## Use

Ask something like "Help me submit this software contract to BuyND+" and attach the documents. The assistant takes it from there.

## Maintaining

When the BuyND+ form changes, update `references/buynd-form-fields.md`. Its source is the *Contract Request Questions Inventory* spreadsheets in the web app repo (`docs/`). Bump `metadata.version` in `SKILL.md` with each change.

## Disclaimer

This skill does not approve contracts and does not replace any part of the review process. ND Procurement and General Counsel review every contract. Don't put contract documents into AI tools that aren't approved for the data they contain.
