# 🎩 Farcaster FollowCheck Mini-App

> A professional, mobile-optimized Farcaster Mini-App to instantly check who is not following you back. Built with Next.js 15, Neynar API, and Farcaster SDK.

![App Preview](public/logo.png)

## ✨ Features

- **🔒 Instant Auth:** Automatically detects Farcaster user via SDK Context (SIWN).
- **🚀 Smart Analysis:** Scans thousands of followers using Neynar API pagination (handles large accounts easily).
- **📱 Mobile Native:** Uses deep links (`sdk.actions.openUrl`) to open profiles directly inside Warpcast.
- **🎨 Premium UI:** Glassmorphism design, smooth animations, and dark mode.
- **🛡️ Secure:** No wallet signature required for basic checks.

---

## ⚡ Quick Start (Deploy in 2 Minutes)

You can deploy your own version of this app to Vercel with one click:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fcoinisan%2Ffarcaster-follow-checker&env=NEYNAR_API_KEY,NEXT_PUBLIC_ONCHAINKIT_API_KEY)

### Post-Deploy Configuration (Crucial Step)
After deploying, you **MUST** update the Manifest file to match your new Vercel domain.

1. Go to your code (in GitHub or Vercel Edit Mode).
2. Open `app/.well-known/farcaster.json/route.ts`.
3. Change `const appUrl` to your new domain:
   ```typescript
   // Change this to YOUR Vercel URL
   const appUrl = "[https://your-project-name.vercel.app](https://your-project-name.vercel.app)";
