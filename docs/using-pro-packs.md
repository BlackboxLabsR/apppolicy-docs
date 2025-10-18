# Using Pro Rule Packs

Pro rule packs add broad iOS & Android coverage for App Store/Play policy requirements.

## Verification

Each pack is:
- **Signed** with AppPolicy’s private key (Ed25519)
- **Verified** in your CI using your pinned `APPPOLICY_PUBKEY_HEX`

If verification fails, evaluation stops:
```
Signature FAILED: Signature was forged or corrupt
```

## Updating Packs

1. Packs are tagged monthly (`rules-vYYYY.MM.DD`).
2. Replace the `rules_pack_url` with the latest release asset.
3. The Action verifies signature automatically and continues.

## Local validation (optional)

```bash
python -m apcop.pro_pack verify ./rules-pack-2025.10.24.tar.gz
```