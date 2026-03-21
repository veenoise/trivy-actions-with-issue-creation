---
title: "Security Alert ({{ env.GITHUB_REF_NAME }}): High/Critical Vulnerabilities Found"
name: "Security Alert ({{ env.GITHUB_REF_NAME }}): High/Critical Vulnerabilities Found"
about: "High or Critical vulnerabilities found in branch {{ env.GITHUB_REF_NAME }}. Review the scan report and patch affected dependencies to maintain security compliance."
labels: [ "security", "bug" ]
---

### 🛡️ Trivy Scan Results
High or Critical vulnerabilities were detected during the automated filesystem scan.

**Workflow Details:**
- **Run ID:** {{ env.GITHUB_RUN_ID }}
- **Branch:** {{ env.GITHUB_REF_NAME }}
- **Triggered By:** @{{ env.GITHUB_ACTOR }}

---

### 📊 Scan Output (Table)
```text
{{ env.REPORT_DATA }}
```

### 📋 Action Required
Please review the logs in the GitHub Actions tab to see the full table output:
[View Workflow Run]({{ env.GITHUB_SERVER_URL }}/{{ env.GITHUB_REPOSITORY }}/actions/runs/{{ env.GITHUB_RUN_ID }})

**Summary of Scan Configuration:**
- **Scanners:** `vuln`
- **Severity:** `HIGH, CRITICAL`
- **Ignore Unfixed:** `true`

> [!IMPORTANT]
> Vulnerabilities with no known patch have been ignored. The issues listed in the logs require manual intervention or version upgrades.
