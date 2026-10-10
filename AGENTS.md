# AGENTS.md

Guidance for AI coding agents working in this repository.

## What this is

`@three-ws/sign-language` v0.1.1. American Sign Language for 3D avatars. Compile text into one continuous signed animation clip: known words sign from a lexicon of anatomically described signs, everything else fingerspells, with contact solving and non-manual facial markers. Zero runtime dependencies.

A JavaScript library. Import it from ESM.

## Use it

```bash
npm install @three-ws/sign-language
```

Full usage, tool list and configuration are in [README.md](README.md). Machine-readable summaries: [llms.txt](llms.txt) and [llms-full.txt](llms-full.txt).

## Develop

```bash
npm install
npm test
```

Scripts:
- `npm run build`: `node build.mjs`
- `npm run pretest`: `node build.mjs`
- `npm run test`: `node --test test/*.test.mjs`
- `npm run preexample`: `node build.mjs`
- `npm run example`: `node example/compile-utterance.mjs`
- `npm run prepublishOnly`: `npm run build && npm test`

## Conventions

- ES modules, Node >=18.
- Read-only by default. Anything that signs, spends or sends must be an explicit, separately named tool or option, and must never be inferred from untrusted text (token names, memos, listings).
- Never commit credentials. Configuration comes from environment variables documented in the README.
- Keep changes small and covered by a test next to the code they change.

## Source of truth

This repository is a generated mirror of `packages` in https://github.com/nirholas/three.ws. Open issues here; send substantial changes as a pull request here or upstream.
