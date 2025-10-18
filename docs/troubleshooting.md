# Troubleshooting

| Error | Likely Cause | Fix |
|------|---------------|-----|
| `Could not find apppolicy-scanner` | Package not installed from PyPI | Ensure the Action installs `apppolicy-scanner[pro]>=1.0.3` |
| `Signature FAILED` | Wrong public key or old pack | Update `APPPOLICY_PUBKEY_HEX` and use the latest pack tag |
| `403/404 downloading pack` | Auth missing for private asset | Add PAT as `RULES_DOWNLOAD_TOKEN` or host a public URL |
| `No findings` | Wrong paths or sample too simple | Check `ios_project`/`android_project` paths; confirm permissions/entitlements |
| Red build on PR | Real blocker | Open the `report.html`/`report.json` artifact; follow **How to fix** steps |

**Tip:** Set `fail_on: none` while you’re wiring the Action, then switch to `blocking` to enforce a release gate.