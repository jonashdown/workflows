# Commit to Develop

## DONT DO THIS!

```
DONT DO THIS
```

Code changes are commited directly to the develop branch, code can be either cherry-picked or selected from a commit and deployed to a lower level environment. Cherry-picked code is released to production

```mermaid
gitGraph
  commit
  branch develop
  commit
  commit id: "Feature 1"
  commit
  commit
  checkout main
  cherry-pick id: "Feature 1"
  checkout develop
  merge main
  commit
  commit
  commit
  commit id: "Feature 2"
  commit
  commit
  commit
  commit
  commit
  commit
  commit id: "Feature 3"
  checkout main
  cherry-pick id: "Feature 3"
  checkout develop
  merge main
  commit
  commit
  commit
  checkout main
  cherry-pick id: "Feature 2"

```