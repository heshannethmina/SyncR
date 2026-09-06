<div align="center">
  <img src="web/public/syncr-logo.png" alt="SyncR" width="260" />

  <p><strong>A focused, real-time code interview workspace.</strong></p>

  <p>
    <a href="https://github.com/heshannethmina/SyncR/actions/workflows/ci.yml"><img src="https://github.com/heshannethmina/SyncR/actions/workflows/ci.yml/badge.svg" alt="CI status" /></a>
    <a href="#contributing">Contribute</a>
  </p>
</div>

## What is SyncR?

SyncR makes technical interviews feel natural: an interviewer creates a room, shares an invite link, and collaborates with a candidate in the same code editor in real time. Candidates can join from their browser—no installation or account required.

It is designed for startups, hiring teams, and university placement programmes that want a lightweight alternative to larger interviewing platforms.

## Product highlights

- Live shared code editing with room-based invite links
- Browser-based coding workspace powered by the Monaco editor
- Multi-language code execution via Judge0 when an execution service is connected
- Interview dashboard for creating and managing rooms
- Secure accounts, sessions, and room access
- Admin tools for promotion codes and account plans

## Built with

| Area | Technologies |
| --- | --- |
| Frontend | Next.js, React, TypeScript, Tailwind CSS, Monaco Editor |
| Backend | Go, Gorilla WebSocket |
| Data | PostgreSQL |
| Code execution | Judge0 |
| Deployment | Vercel and Render |
| Quality | GitHub Actions, ESLint, Go tests |

## Repository guide

| Path | Purpose |
| --- | --- |
| `web/` | Next.js application and the product interface |
| `backend/` | Go API, WebSocket collaboration service, and data layer |
| `docs/` | Project documentation and route map |
| `.github/` | Automated checks and dependency maintenance |

## Contributing

Contributions, bug reports, and product ideas are welcome. **[CONTRIBUTING.md](CONTRIBUTING.md)** has the full guide: how to get both halves running locally, the two checks that skip themselves silently, and what review expects.

The short version:

1. Search the [issues](https://github.com/heshannethmina/SyncR/issues) first. Anything tagged `good first issue` is genuinely self-contained.
2. Ask in [Discussions](https://github.com/heshannethmina/SyncR/discussions) rather than filing an issue if you are not yet sure it is one. Anything that changes the WebSocket protocol, the schema or the concurrency design should start as a **design proposal** there.
3. One branch per change, branched from `main`. Merged branches are kept, but a branch is done once its pull request merges — start a new one rather than reusing it.
4. Pull request titles are conventional commits (`fix: stop the caret jumping`) — squash merging makes the title the commit message on `main`, and a workflow checks it.
5. Link the issue with `Closes #123` in the description. Closing keywords only fire at merge time.

[`CLAUDE.md`](CLAUDE.md) is the design record — why one goroutine owns each document, why tokens are not JWTs, why Python runs in the browser. Read the relevant part before proposing a change to any of it; several of those choices look like accidents and are not.

## Community

A good place to start is the interface, documentation, accessibility, tests, or the interview workflow itself. Please be kind, specific, and collaborative — see the [Code of Conduct](CODE_OF_CONDUCT.md).

Security problems go to a [private advisory](https://github.com/heshannethmina/SyncR/security/advisories/new), never a public issue. The [security policy](.github/SECURITY.md) explains what is in scope and what is deliberately not.

---

Built for better technical conversations.

> **Note:** The contact details in `web/components/Footer.tsx` (`CONTACT_PLACEHOLDER`) are placeholders. Remove or replace them with real details before deploying — a footer with no contact column is better than one with invented contact information.
