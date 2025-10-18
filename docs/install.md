# Install — Community & Pro

## Option A — Community (Free)

Add the Action and point to a community rules file in your repo.

```yaml
- uses: BlackboxLabsR/apppolicy-sdks@v1
  with:
    ios_project: ios/
    android_project: android/
    rules_path: rules/community.yaml
    fail_on: advisory
```

## Option B — Pro Rules Pack (Signed)

1. Get your **Pro pack URL** and **Public Key (hex)** from AppPolicy support.
2. Store the public key in CI secrets:
   ```text
   APPPOLICY_PUBKEY_HEX = <hex-value>
   ```
3. Use the Action with `rules_pack_url` and `public_key_hex`:

```yaml
- uses: BlackboxLabsR/apppolicy-sdks@v1
  with:
    ios_project: ios/
    android_project: android/
    rules_pack_url: https://releases.example.com/rules-pack-2025.10.24.tar.gz
    public_key_hex: ${{ secrets.APPPOLICY_PUBKEY_HEX }}
    fail_on: blocking
```

On PRs you’ll get a `report.json` artifact (and optional HTML report) explaining **Why** each finding matters and **How** to fix it.