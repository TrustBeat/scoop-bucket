# TrustBeat Scoop bucket

[Scoop](https://scoop.sh) manifests for [TrustBeat](https://trustbeat.eu/en) —
digital trust infrastructure for the EU.

```powershell
scoop bucket add trustbeat https://github.com/TrustBeat/scoop-bucket
scoop install trustbeat
```

## What's here

| Manifest | Description |
|---|---|
| `trustbeat` | CLI that anchors files to qualified eIDAS timestamps and verifies the proofs offline |

## Verifying what you installed

The manifest pins the SHA-256 of the release archive, and Scoop checks it on
download. Those same artifacts are anchored with a qualified timestamp by the
release workflow, so the binary Scoop puts on your machine is the one that was
timestamped.

`trustbeat verify` needs no network connection and no API key — a proof stays
verifiable offline for as long as you keep it.

## Updating the manifest

`checkver` and `autoupdate` are wired to the
[trustbeat-cli releases](https://github.com/TrustBeat/trustbeat-cli/releases),
so a new version can be picked up automatically:

```powershell
.\bin\checkver.ps1 trustbeat -u
```

The hash is read from each release's `SHA256SUMS` asset rather than being
recomputed, so the manifest records exactly what the release published.

## Beyond the CLI

The CLI anchors files. The same qualified-timestamp infrastructure also backs:

| | |
|---|---|
| [Tamper-Evident Logs](https://trustbeat.eu/en/products/tamper-evident-logs) | Sealed log trails for NIS2 Article 21 |
| [AI Decision Anchoring](https://trustbeat.eu/en/products/ai-decision-anchoring) | Provable records of model decisions |
| [Audit Trail](https://trustbeat.eu/en/products/audit-trail) | Append-only, independently verifiable event history |
| [EU Digital Identity](https://trustbeat.eu/en/products/eu-digital-identity) | EUDI Wallet / eIDAS 2 credential verification |
| [Signature Verification](https://trustbeat.eu/en/verify-signature) | Full qualified-status assessment against the EU Trusted List |

Prefer a library? Python, TypeScript, Java, C# and Go SDKs:
**[trustbeat.eu/en/sdks](https://trustbeat.eu/en/sdks)**.

Free tier — 100 anchors a month, no card:
**[trustbeat.eu/en/pricing](https://trustbeat.eu/en/pricing)**.

## Source

The manifests are maintained in the TrustBeat monorepo and mirrored here — open
issues and pull requests against
[TrustBeat/trustbeat-cli](https://github.com/TrustBeat/trustbeat-cli).
