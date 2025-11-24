🎩 Farcaster FollowCheck Mini-App

> A professional, mobile-optimized Farcaster Mini-App to instantly check who is not following you back. Built with Next.js 15, Neynar API, and Farcaster SDK.

![App Preview](public/logo.png)

 Features

- **🔒 Instant Auth:** Automatically detects Farcaster user via SDK Context (SIWN).
- **🚀 Smart Analysis:** Scans thousands of followers using Neynar API pagination (handles large accounts easily).
- **📱 Mobile Native:** Uses deep links (`sdk.actions.openUrl`) to open profiles directly inside Warpcast.
- **🎨 Premium UI:** Glassmorphism design, smooth animations, and dark mode.
- **🛡️ Secure:** No wallet signature required for basic checks.

---

 Quick Start (Deploy in 2 Minutes)

You can deploy your own version of this app to Vercel with one click:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fcoinisan%2Ffarcaster-follow-checker&env=NEYNAR_API_KEY,NEXT_PUBLIC_ONCHAINKIT_API_KEY)

Post-Deploy Configuration (Crucial Step)
After deploying, you **MUST** update the Manifest file to match your new Vercel domain.

1. Go to your code (in GitHub or Vercel Edit Mode).
2. Open `app/.well-known/farcaster.json/route.ts`.
3. Change `const appUrl` to your new domain:
   ```typescript
   // Change this to YOUR Vercel URL
   const appUrl = "[https://your-project-name.vercel.app](https://your-project-name.vercel.app)";

   

🛠️ Manual Installation (For Developers)
If you want to run it locally or contribute:


1. Clone the Repository
Bash
git clone [https://github.com/coinisan/farcaster-follow-checker.git](https://github.com/coinisan/farcaster-follow-checker.git)
cd farcaster-follow-checker

2. Install Dependencies
Bash
npm install

3. Set Up Environment Variables
Rename .env.example to .env.local and fill in your keys:
Bash
cp .env.example .env.local
-
How to get keys:
NEYNAR_API_KEY: Go to Neynar.com, sign up, and get an API Key from the dashboard. Note: A "Starter" plan is recommended for fetching large follower lists.
NEXT_PUBLIC_ONCHAINKIT_API_KEY: Go to Coinbase Developer Platform, create a project, and copy the Client Key.

4. Run Locally
Bash
npm run dev
Open http://localhost:3000. Tip: Use the "Demo Mode" button to test the UI without a Farcaster connection.


How to Validate & Share
To make your app visible inside Farcaster (Warpcast):

1-Go to Warpcast Frame Developer Tools.
2-Enter your app URL (e.g., https://your-app.vercel.app).
3-Click Validate.
4-Once validated, you can share the link in a cast, and it will appear as a Mini-App!

Project Structure
- /app/page.tsx -> Main UI & Logic (Client Side).
- /app/api/unfollowers/route.ts -> Backend logic (Fetches data from Neynar).
- /app/.well-known/farcaster.json/route.ts -> Farcaster Manifest (Identity card of the app).

Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.

License
This project is licensed under the MIT License.
