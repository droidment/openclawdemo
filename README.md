# OpenClaw Demo

Hacker/terminal-style landing page for the OpenClaw meetup demo.

## Local preview

Open `index.html` in a browser.

You can also serve it locally:

```bash
python3 -m http.server 8000
```

## Repo intent

A lightweight static page that showcases:

- chat-native automation
- trigger-based workflows
- group summaries
- operator-console vibes for demos
- app subpages like Raj Bala's Health Tracker

## Firebase Hosting auto deploy

This repo includes:

- `.firebaserc` with the default Firebase project
- `firebase.json` for static Hosting config
- Firebase CLI-generated GitHub Actions workflows for Hosting deploys

What happens after you push:

- Pull requests deploy to a Firebase Hosting preview channel
- Pushes to `main` deploy to the live Hosting site

GitHub repository secrets you need to add:

- None manually if you use `firebase init hosting:github`

Recommended setup:

1. Install the Firebase CLI if needed.
2. Run `firebase login`.
3. Run `firebase init hosting` in this repo and select your Firebase project.
4. Run `firebase init hosting:github` to let Firebase create the service account, upload the GitHub secret, and generate the deploy workflows.

Once the generated workflow files are pushed to GitHub, every pull request gets a preview deploy and every push to `main` auto-deploys live.
