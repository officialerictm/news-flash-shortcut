# News‑Flash Shortcut 🚀

**One‑tap AI digest + omni‑channel posting.**  
Share any article → get a concise, nuanced summary → blast it to Threads, X (Twitter), Bluesky, Mastodon, LinkedIn, or email. Need a deeper take? “Write a Think‑Piece” spawns a WordPress‑ready draft.

This repo hosts:
* `unsigned/News‑Flash_FullBuild.shortcut` – the raw shortcut (no Apple signature).
* `.github/workflows/sign‑shortcut.yml` – GitHub Actions job that notarizes and re‑signs the shortcut so iOS will install it.

## How to get the signed build

1. Fork or clone the repo.  
2. In repo **Settings → Secrets → Actions** add two secrets:  
   * `APPLE_ID` – any Apple ID email  
   * `APPLE_PASSWORD` – **app‑specific** password (generate at appleid.apple.com)  
3. Back in **Actions** tab, run **Sign & Release Shortcut**.  
4. Download the artifact *News‑Flash.signed.shortcut* and tap it on your iPhone → “Add Shortcut”.

Ready to use.

---

### Folder structure

unsigned/
└── News‑Flash_FullBuild.shortcut # stays unsigned here
.github/
└── workflows/
└── sign‑shortcut.yml # notarize + sign

---

### Contributing

* OpenAI prompts live inside the shortcut—feel free to tweak tone, word limits, or add new social branches (e.g., LinkedIn article mode).
* PRs welcome. Please run `npm run lint` on YAML if you touch the workflow.

---

MIT © 2025 Eric Martin
