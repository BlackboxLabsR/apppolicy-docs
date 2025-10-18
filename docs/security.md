# Security & Data Model

- **Local-first**: Source code never leaves your CI environment.
- **Facts only**: The scanner extracts manifest/entitlement/SDK facts; no code content is transmitted.
- **Signed Pro Rule Packs**: Pro packs are signed (Ed25519). CI verifies with your pinned `APPPOLICY_PUBKEY_HEX`.
- **Zero telemetry**: AppPolicy does not collect scan data by default.
- **Key rotation**: You can rotate your pinned public key; new packs are signed accordingly.