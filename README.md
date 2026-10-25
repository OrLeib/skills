# skills

[![skills.sh](https://skills.sh/b/orleib/skills)](https://skills.sh/orleib/skills)

Production patterns for AI coding agents. One folder per skill. Add another folder when the next hard-won failure mode is worth teaching; do not open a new GitHub repo for it.

Install one skill:

```bash
npx skills add orleib/skills --skill session-verdict
```

Install every skill in the pack:

```bash
npx skills add orleib/skills
```

## Skills

| Skill | Use when |
| --- | --- |
| [session-verdict](./session-verdict/) | Capacitor WebView + supabase-js: empty `getSession`, storage still warming, or a network error treated as logout. Upgrade to 2.108.2+ for the old phantom `SIGNED_OUT` bug. |
| [ai-coding-interview](./ai-coding-interview/) | Live AI-enabled coding interview: the agent pairs as a concise partner (grill, small slices, a defense list per slice, show it running). [PREP.md](./ai-coding-interview/PREP.md) is the candidate's checklist. |
| [capacitor-app-icons](./capacitor-app-icons/) | Capacitor app on macOS: generate every iOS, Android and PWA icon size and splash screen from one 1024x1024 image, with no dependencies beyond the built-in `sips`. |

## License

MIT
