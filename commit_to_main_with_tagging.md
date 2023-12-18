# Commit to Main With Tagging

## DONT DO THIS!

```
DONT DO THIS
```

Code changes are commited directly to the main branch, git tags ares created when features are complete and deployed to lower level environments periodicallly. Git tags are selected and released to production periodcally.

```mermaid
gitGraph
  commit
  commit
  commit id: "Feature 1" tag: "1.0.0"
  commit
  commit
  commit
  commit
  commit
  commit
  commit id: "Feature 2" tag: "1.0.1"
  commit
  commit
  commit
  commit
  commit
  commit
  commit id: "Feature 3" tag: "1.0.2"

```