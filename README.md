# GuardSec Browser Extension

GuardSec is a Chrome Manifest V3 extension for passive browser-side security
observation. It does not actively probe or block websites. Deeper active assessment
occurs through the GuardSec backend only after authentication, required ownership
verification, authorization attestation, and scope checks.

The extension is distributed manually, not through the Chrome Web Store. No Chrome
Web Store approval is claimed.

## Install

Download the extension ZIP and checksum from [GitHub Releases](https://github.com/Serdyznet1/GuardSec-Extension-Releases/releases/tag/v0.1.0), then follow
[the installation instructions](INSTALL.md). GitHub's automatically generated
"Source code" archives contain these documents, not the installable extension.

The product origin is [guardsec.online](https://guardsec.online). Local passive
observation does not require an account; authenticated features require the
GuardSec service to be available.

## Release provenance

- Extension version: **0.1.0**
- Private GuardSec source commit: `8f17ac64c14c354676c3fdd20b7a07de3b7b1891`
- Package: `guardsec-extension-v0.1.0.zip`
- SHA-256: `6b219d0c695d131905961624de36533750b5fd2de2d938b3664f8b4b3a5dc0a5`

This is an independent public distribution repository. The application source
repository and its history remain private; the source commit above identifies
provenance and is not publicly inspectable here. The release tag identifies the
public documentation commit, not the private source commit. Only compiled runtime
assets and public documentation are distributed.

## Dependency review for this release

The reviewed dependency audit reported 24 affected package entries (19 high and
5 moderate), all in development/build tooling: ESLint and its YAML/glob dependencies;
Vite, its plugins and Tailwind/PostCSS dependencies; and Vitest/mocking tooling.
These tools participate in development or compilation, but their reported vulnerable
code is not shipped in the extension runtime. Inspection of rendered bundle modules
identified only React, React DOM and Scheduler as third-party runtime packages;
the production-dependency audit reported zero findings. This is a release-specific
review, not a guarantee against undiscovered vulnerabilities. No dependencies were
upgraded for this release.

The source's existing `eslint.config.js` formatting check failure was recorded
separately; that tooling configuration is not included in the package.
