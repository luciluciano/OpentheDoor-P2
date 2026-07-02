# OpentheDoor:P2 — Interactive Security Field Manuals

Single-file, no-build HTML reference guides for common security tools. Each page is a self-contained interactive manual — searchable command tables, expandable sections, and a printable cheat sheet — designed to be read in-browser or hosted straight off GitHub Pages.

**Live reference series:**

| Part | Tool | File |
|------|------|------|
| 01 | Nmap — network discovery & recon | [`nmap/index.html`](./nmap/index.html) |
| 02 | Metasploit — exploitation framework | [`metasploit/index.html`](./metasploit/index.html) |

> Adjust the folder names/paths above to match however you organize the repo — see [Suggested structure](#suggested-structure) below.

## What's inside each manual

- **Foundations** — what the tool is, how it fits into a wider workflow, and how to install it
- **Command anatomy** — the building blocks of a typical invocation, broken into copy-pasteable pieces
- **Searchable reference console** — every flag/command indexed with what it does, what it touches, and how "loud" it is
- **Deep-dive sections** — scripting engines, module types, payloads, timing/performance tuning
- **Evasion concepts** — explained at a conceptual level (what problem the technique solves, what it's detected by) rather than as ready-to-run bypass code
- **Legal & ethics checklist** — an interactive, click-to-check list to run through before every engagement
- **Cheat grid** — the handful of one-liners you'll actually reach for day to day

## Running it

No build step, no dependencies, no server required.

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
open nmap/index.html          # macOS
xdg-open metasploit/index.html # Linux
start metasploit/index.html    # Windows
```

Or just double-click the HTML file in a file browser — everything (fonts aside) runs client-side.

### Hosting on GitHub Pages

1. Settings → Pages → Deploy from branch → `main` → `/ (root)`
2. Visit `https://<your-username>.github.io/<your-repo>/nmap/` or `/metasploit/`

## Suggested structure

```
.
├── README.md
├── nmap/
│   └── index.html
└── metasploit/
    └── index.html
```

## Tech

Plain HTML/CSS/JS — no framework, no bundler. Fonts load from Google Fonts (Space Grotesk, Inter, JetBrains Mono); everything else is inline so each file works completely offline once fonts are cached.

## Scope & intent

These are **reference and study material** — the same level of detail you'd find in official tool documentation, vendor blogs, or OSCP-style course notes: command syntax, module taxonomy, and workflow, not weaponized exploit code or ready-to-run attack chains. They're built for students and authorized penetration testers to study *how* these tools are structured, not as a substitute for reading the official docs before an engagement.

## ⚠️ Legal notice

Only run any command shown in these manuals against:
- Systems you own, **or**
- Systems you have explicit, written authorization to test (e.g. a signed rules-of-engagement document), **or**
- Purpose-built legal practice targets (Metasploitable2, TryHackMe, HackTheBox, PortSwigger Academy, etc.)

Scanning, exploiting, or otherwise testing systems without authorization is illegal in most jurisdictions, regardless of intent. The maintainers of this repository are not responsible for misuse.

## Contributing

Found an outdated flag, a broken link, or want to add another tool as "Part 03"? PRs and issues welcome — keep new entries at the same conceptual/reference level described above.

## License

MIT — see [`LICENSE`](./LICENSE) for details. (Add a `LICENSE` file if one isn't in the repo yet.)

---

Built by Devadath C.
