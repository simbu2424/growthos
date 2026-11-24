GROWTHOS WEBSITE — PREVIEW BUILD
================================

This is the first website preview for GrowthOS. It is a responsive static website/PWA that can be hosted free on GitHub Pages. It does not require a public IP address or a purchased domain.

IMPORTANT SECURITY NOTICE
-------------------------
This preview currently stores app data in browser localStorage without local encryption. The OneDrive sign-in/sync workflow is intentionally not enabled in this preview. Use sample/test data only. Do not enter real financial records, private journal entries, passwords, health information, or other sensitive data.

PUBLISH WITH GITHUB PAGES (FREE)
--------------------------------
1. Create or sign in to a GitHub account at https://github.com.
2. Create a NEW public repository named: growthos
3. Upload the CONTENTS of this folder to the repository root (index.html, manifest.webmanifest, sw.js, 404.html, .nojekyll, .github/).
4. In the repository, open Settings > Pages.
5. Under Build and deployment, choose GitHub Actions. The included workflow deploys the static site.
6. Wait for the workflow to finish. GitHub Pages will show your website address, usually:
   https://YOUR-GITHUB-USERNAME.github.io/growthos/
7. Open the address on your Windows PC. On Android, open it in Chrome and choose Install app / Add to Home screen.

NO PUBLIC IP OR DOMAIN NEEDED
-----------------------------
GitHub Pages hosts the static website over HTTPS. The GitHub-provided address is enough for the first version. Do not add a custom domain or DNS records.

PERSONAL MICROSOFT ACCOUNT / ONEDRIVE
-------------------------------------
After the GitHub Pages URL exists, use that exact HTTPS origin/redirect URL when registering the Microsoft application for personal Microsoft accounts. The app registration must use a public-client/SPA flow with PKCE and delegated least-privilege permissions. Never place a client secret in this website. We will configure the client ID and exact redirect URI only after the final website URL is known.

OneDrive sync is NOT implemented/validated in this preview. Before enabling it, we must replace plaintext local storage, review XSS and import validation, implement robust conflict handling and recovery, test real Microsoft sign-in on desktop/mobile, and arrange an independent penetration test.

LOCAL PREVIEW (OPTIONAL)
------------------------
From this folder run:
  python -m http.server 8000
Then open:
  http://localhost:8000

The app is a prototype. A source-level package check is not a runtime security test or penetration test.
