# Install GuardSec v0.1.0 in Chrome

The ZIP is a transport package for Chrome's **Load unpacked** workflow, not a
one-click installer. GuardSec is not currently distributed through the Chrome Web
Store.

1. Open [release v0.1.0](https://github.com/Serdyznet1/GuardSec-Extension-Releases/releases/tag/v0.1.0)
   and download **guardsec-extension-v0.1.0.zip** and its **.zip.sha256** file.
   Do not select GitHub's "Source code" archives.
2. Optionally verify the ZIP's SHA-256 against the supplied checksum:
   - PowerShell: `Get-FileHash .\guardsec-extension-v0.1.0.zip -Algorithm SHA256`
   - Linux: `sha256sum -c guardsec-extension-v0.1.0.zip.sha256`
3. Extract the ZIP into a permanent folder.
4. Open `chrome://extensions` in desktop Google Chrome.
5. Enable **Developer mode**.
6. Select **Load unpacked**.
7. Choose the extracted GuardSec directory with **manifest.json at its root**.

Optionally pin GuardSec in Chrome's Extensions menu. Browse an ordinary HTTP/HTTPS
page, open the popup, and select **More Info** for the side panel. Chrome internal
pages are not observation targets.

GuardSec observes information the browser already received. It does not actively
probe or block websites, and it does not capture arbitrary response bodies.
Passive observation works without signing in. The product origin is
[https://guardsec.online](https://guardsec.online); sign in inside GuardSec when
the service is available to use authenticated features. Installation itself does
not require the service to be online. Do not start an active scan just to test
installation.

Access and refresh tokens are stored in `chrome.storage.local`. The WebSocket uses
an access-token query parameter. Keep credentials, raw network traces and
token-bearing URLs private.

## Update or remove

For an update, replace the old extracted contents with the replacement release
and click **Reload** on GuardSec in `chrome://extensions`. Keep the selected
folder at its permanent location. To uninstall, select **Remove** there.

## Provenance and checksum

Version: **0.1.0**. Built from private GuardSec source commit
`8f17ac64c14c354676c3fdd20b7a07de3b7b1891`; public users cannot inspect that private
commit through this repository.

Expected ZIP SHA-256:

```text
6b219d0c695d131905961624de36533750b5fd2de2d938b3664f8b4b3a5dc0a5
```
