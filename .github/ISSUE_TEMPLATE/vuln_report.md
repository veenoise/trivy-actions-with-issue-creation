---
title: "Security Alert: High/Critical Vulnerabilities Found"
assignees: [ "" ]
labels: [ "security", "bug" ]
---

### 🛡️ Trivy Scan Results
High or Critical vulnerabilities were detected during the automated filesystem scan.

**Workflow Details:**
- **Run ID:** {{ env.GITHUB_RUN_ID }}
- **Branch:** {{ env.GITHUB_REF_NAME }}
- **Triggered By:** @{{ env.GITHUB_ACTOR }}

---

### 📋 Action Required
Please review the logs in the [GitHub Actions tab](${{ env.GITHUB_SERVER_URL }}/${{ env.GITHUB_REPOSITORY }}/actions/runs/${{ env.GITHUB_RUN_ID }}) to see the full table output of the scan.

**Summary of Scan Configuration:**
- **Scanners:** `vuln`
- **Severity:** `HIGH, CRITICAL`
- **Ignore Unfixed:** `true`

> [!IMPORTANT]
> Vulnerabilities with no known patch have been ignored. The issues listed in the logs require manual intervention or version upgrades.