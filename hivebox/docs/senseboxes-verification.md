# SenseBoxes Verification Log

**Date Verified:** 2025-09-16  
**Verification Method:** API calls via `curl` and `verify_senseboxes.py`

---

## Verified Boxes

| Alias         | Box ID                    | Status | Name (API)        | Sensors | Notes                      |
|---------------|--------------------------|--------|------------------|--------|---------------------------|
| Site A        | 5eba5fbad46fb8001b799786 | ✅ 200 | (fetched via API) | n/a    | Used for Phase 3 testing  |
| Site B        | 5c21ff8f919bf8001adf2488 | ✅ 200 | (fetched via API) | n/a    | Outdoor reference box     |
| Site C        | 5ade1acf223bd80019a1011c | ✅ 200 | (fetched via API) | n/a    | Indoor calibration box    |

---

## Sample Verification Command
```bash
curl "https://api.opensensemap.org/boxes/5eba5fbad46fb8001b799786" | ConvertFrom-Json | Select-Object -Property name, sensors
curl "https://api.opensensemap.org/boxes/5c21ff8f919bf8001adf2488" | ConvertFrom-Json | Select-Object -Property name, sensors
curl "https://api.opensensemap.org/boxes/5ade1acf223bd80019a1011c" | ConvertFrom-Json | Select-Object -Property name, sensors

-- 

✅ **Purpose**: Human-readable verification log for project reviewers & stakeholders.  
✅ **Good practice**: include date/time, commands used, and result summary for traceability.

---

## 3) (Optional) GitHub Actions Workflow – Continuous Verification  
Add to `.github/workflows/verify-senseboxes.yml` if you want automated checks on push:

```yaml
name: Verify SenseBoxes
on:
  workflow_dispatch:
  push:
    branches: [ main ]

jobs:
  verify:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Set up Python
        uses: actions/setup-python@v5
        with:
          python-version: '3.x'
      - name: Install dependencies
        run: pip install requests
      - name: Run verification script
        run: python verify_senseboxes.py
