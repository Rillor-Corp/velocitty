# Velocitty

Velocitty is an SSH terminal for the Mac that an AI can work in under rules you sign. It keeps your servers and logins in
a built-in vault, and an AI runs a command on a server only when your rules, or you, allow it. Velocitty is a beta.

This repository holds the releases only. The source code is not distributed.

## Download

- The newest version: <https://github.com/Rillor-Corp/velocitty/releases/latest/download/Velocitty_universal.dmg>
- Every version, with its notes: <https://github.com/Rillor-Corp/velocitty/releases>
- The website: <https://velocitty.com>

Velocitty needs macOS 12 or later. It has been run on Apple silicon Macs with macOS 26 only. Intel Macs are not supported
yet. Windows and Linux are coming soon.

Open the disk image and drag Velocitty into Applications. Keep one copy of the app only. After that, updates arrive inside
the app: Settings, About, Check for updates.

## Check a download

The disk image and the `velo` downloads each have a `.sha256` file beside them.

1. Download `Velocitty_universal.dmg` and `Velocitty_universal.dmg.sha256` into the same folder. In Terminal, in that
   folder:

   ```
   shasum -a 256 -c Velocitty_universal.dmg.sha256
   ```

   It must answer `Velocitty_universal.dmg: OK`.

2. After you install it, ask macOS who signed the app and whether Apple checked it:

   ```
   spctl -a -vvv -t exec /Applications/Velocitty.app
   codesign --verify --deep --strict --check-notarization -R=notarized /Applications/Velocitty.app
   ```

   The first must say `accepted`, `source=Notarized Developer ID` and a signer that ends in `(5F725G736M)`. The second
   must print nothing.

If either check fails, do not open the app. Delete the download and write to us (below).

`velo`, the command-line tool, is inside the app. Its separate downloads on a release (`velo-…-apple-darwin.tar.gz`) are
for a machine without the app, and are checked the same way with their `.sha256` files.

## Remove Velocitty

1. If you set up Downforce (Vault, Downforce protected Vault), remove it first from the same card: Manage installation,
   Remove Downforce. It asks for your administrator password. One thing stays: a hidden macOS account that is switched off
   and empty, because macOS does not let an app delete an account.
2. Quit Velocitty and move it from Applications to the Trash.
3. Your servers, vault and settings are in `~/Library/Application Support/com.velocitty.desktop` and `~/.velocitty`.
   Delete these two folders only if you want that data gone for good. Keep them and a later install finds everything
   again. Two small things may stay in your keychain: a key for the vault, if you chose the Secure Enclave, and a marker
   for your signed AI rules. Neither holds your data, and neither is of use without the folders above.

## Help

- A problem or a question: <hello@velocitty.com>
- A security issue: <security@velocitty.com> (see [SECURITY.md](SECURITY.md))

## Terms and privacy

- Terms of use: <https://velocitty.com/terms/>
- Privacy policy: <https://velocitty.com/privacy/>

By installing or using Velocitty you agree to the terms of use.
