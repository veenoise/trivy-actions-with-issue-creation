---
title: "({{ env.GITHUB_REF_NAME }}) Security Alert: High/Critical Vulnerabilities Found"
name: "Trivy Issue Template"
about: "Automated security alert for High/Critical vulnerabilities found during the CI/CD pipeline scan. Requires immediate review and remediation."
labels: [ "security", "bug" ]
---

### 🛡️ Trivy Scan Results
High or Critical vulnerabilities were detected during the automated filesystem scan.

**Workflow Details:**
- **Run ID:** [{{ env.GITHUB_RUN_ID }}]({{ env.GITHUB_SERVER_URL }}/{{ env.GITHUB_REPOSITORY }}/actions/runs/{{ env.GITHUB_RUN_ID }})
- **Branch:** [{{ env.GITHUB_REF_NAME }}]({{ env.GITHU_SERVER_URL }}/{{ env.GITHUB_REPOSITORY }}/tree/{{ env.GITHUB_REF_NAME }})
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
- **Scanners:** `vuln, secret, misconfig`
- **Severity:** `HIGH, CRITICAL`
- **Ignore Unfixed:** `true`

> [!IMPORTANT]
> Vulnerabilities with no known patch have been ignored. The issues listed in the logs require manual intervention or version upgrades.