# Security policy

Velocitty holds people's SSH keys and passwords, so we want to hear about a weakness before anyone else does.

## How to report

Write to **security@velocitty.com**. Please do not open a public issue or post it anywhere first. If you can, encrypt nothing and
send plain text: we would rather read your report than wait for a key exchange. Use the same address to tell us a copy of our
source code reached you.

## What is in scope

- The **desktop app** (macOS; Windows and Linux builds when released) and **`velo`**, its command-line client and daemon.
- The **phone app** (iOS and Android).
- **Velocitty Cloud**: `app.velocitty.com` (the web app) and `cloud.velocitty.com` (the API).

Out of scope: a server you run yourself; a denial of service by sheer volume; social engineering of our people; findings that need
a rooted or already-compromised device or an attacker who already holds your master password; the third-party services we use
(report those to their owners); and any test against another customer's account or data. Make your own account on Velocitty Cloud
to test, and stop as soon as you can show the problem.

## What to include

- What you found and why it matters (what an attacker gets).
- The app and version (Settings, About), or the address and the time you tried it.
- The steps to reproduce it, or a proof of concept. Please keep a proof from reading, changing or keeping anyone's data.
- Whether you plan to publish, and when.

## What you can expect

- We reply within **3 working days** to say we have your report.
- We give you a first assessment within **10 working days**, and tell you when we have a fix or a date for one.
- We aim to fix a serious problem in Velocitty Cloud within **30 days**, and to ship a fix for the apps in the next release; we will
  tell you if it will take longer and why.
- We credit you in the release notes if you want it, and tell you when the fix is out so you can publish. We ask for **90 days** from your
  report, or until a fix is out, whichever is first, before you publish.

We do not run a bug bounty and promise no payment. We are glad to say thank you in public.

## Safe harbour

If you act in good faith, stay within the scope above, test only your own accounts and data, do not harm other people or the service,
and give us a reasonable time to fix the problem before telling others, we will not start legal action against you and will
say so to anyone who asks. This is a statement of intent, not a licence to break the law or anyone else's rights.
