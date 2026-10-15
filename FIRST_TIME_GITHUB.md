# Onboarding message draft — first-time GitHub setup (for anyone)

Generic onboarding draft. Fill in section 4 per person.
room, your lane is the VRChat loft world — walkable gallery + World Seed
portal room.)

---

**Welcome to the project — GitHub setup from zero** 🥽

**1. Create your GitHub account**
- Go to github.com → Sign up. Pick a username, verify your email. Free, two minutes.
- **Send your username to the project owner** → they add you to the private repo
  (`<owner>/<repo>`). Nothing below works until they do —
  that's step zero.

**2. Make a login token** (GitHub doesn't accept passwords anymore)
- github.com → Settings → Developer settings → Personal access tokens →
  Generate new → check `repo` → copy it somewhere safe. You paste this in as
  your password.

**3. Copy-paste boxes** — open a terminal on your device:

Who you are:
```
git config --global user.name "Your Name"
git config --global user.email "your-github-email"
```

Get the room (login = your username + the token from step 2):
```
git clone https://github.com/<owner>/<repo>.git
cd <repo>
git pull
```

Start your own branch for your work:
```
git checkout -b yourname/my-thing-20261012
```

**4. Your lane**
*[one line per person — what they own, what nobody touches without them]*

**5. The rules (short version)**
- Branches + draft PRs. Never merge without the owner.
- Label everything CANON / PROPOSAL / OPEN — never present a guess as canon.
- Full version lives in the repo: `AGENT_GIT_SETUP.md`

**6. Got an AI assistant on your device? Paste these to it** (one box at a time):

Start here:
```
Hi! I'm setting up GitHub on this device for the first time to join a
project. Walk me through it one step at a time and wait for me between
steps. I'm brand new to this.
```

Open the terminal:
```
Open the terminal where git is set up on this device.
```

No login token yet:
```
I don't have a GitHub personal access token yet. Walk me through
creating one with repo scope.
```

Clone the project (after the owner adds your GitHub username to the repo):
```
Help me clone the private GitHub repo <owner>/<repo>.
```

Check it worked:
```
Check that my git login is working.
```

**7. New to computers? Bring an AI helper.**
- Open ChatGPT (or any AI agent you like) next to this guide and do the
  steps together. The guide + a helper beats the guide alone.
- Paste each box to the helper FIRST and ask "what does this do?" before
  you run it.
- If anything errors, paste the error message to the helper — it will walk
  you through the fix.
- You don't need to understand git. Follow the boxes; the helper explains
  as you go.

Start the helper with this (paste it in):
```
I'm setting up GitHub for the first time to join a project. Walk me through
each step like I'm brand new to computers, one step at a time, and wait for
me before moving on.
```
