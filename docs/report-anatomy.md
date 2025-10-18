# Report Anatomy

This is what you’ll see after a run (downloaded as `report.html`):

- **Header Summary**: counts for **BLOCKING**, **ADVISORY**, and **FYI**.
- **Platform Groups**: iOS and Android findings are grouped.
- **Finding Card**:
  - Severity badge (BLOCKING / ADVISORY / FYI)
  - Rule ID (e.g., `android.target_sdk.minimum`)
  - **Policy** link (points to the official guideline)
  - **Why this matters** (brief context)
  - **How to fix** (concise remediation)
  - **Evidence** (facts used; open the details section)

![Sample report](assets/report-sample.png)

> Tip: You can render HTML locally from the JSON:
>
> ```bash
> apppolicy html --report report.json --out report.html
> ```
