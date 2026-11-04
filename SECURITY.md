# Security

Audio Report AI is a local-first app. It does not operate a server, collect
accounts, or upload audio, transcripts, or reports.

## Reporting a vulnerability

Open a private security advisory through GitHub's **Security → Advisories** tab
for this repository. Do not include patient data, recordings, transcripts,
reports, Apple ID credentials, signing certificates, or other sensitive material
in a public issue.

## Scope

- The app sandbox and local data handling
- The bundled model verification checks
- The IPA packaging and release checksums
- Build and release automation in the private source repository

Signing certificates and Apple ID credentials are handled by your sideloading
tool and Apple. They are not part of this repository or its release assets.
