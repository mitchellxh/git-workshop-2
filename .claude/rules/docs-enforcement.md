---
paths:
  - "scripts/**"
  - "src/**"
---

# Documentation Enforcement

When modifying any file matching these paths:
1. Check the doc-map in CLAUDE.md for the corresponding doc file
2. Update that doc file in the same session
3. Include "Last verified: YYYY-MM-DD" with today's date
4. Add a CHANGELOG.md entry if one doesn't exist for today
