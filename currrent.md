# Current Workflow

Current workflow uses a develop branch. Features are merged into the develop branch, which is deployed to multiple low-level environments. Releases are prepared by cherry-picking merges from the develop branch to the main branch.


```mermaid
gitGraph
  commit
  branch develop
  commit
  checkout main
  commit
  branch feature1
  commit
  checkout main
  commit
  branch feature2
  commit
  commit
  commit
  commit
  checkout develop
  merge feature1
  commit id: "feature1"
  checkout main
  commit
  branch feature3
  commit
  commit
  checkout feature2
  commit
  commit
  checkout feature3
  commit
  checkout develop
  merge feature3
  commit id:"feature3"
  checkout feature2
  commit
  commit
  commit
  checkout main
  cherry-pick id: "feature1"
  checkout feature2
  merge main
  checkout develop
  merge main
  merge feature2
  commit id:"feature2"
  checkout main
  cherry-pick id: "feature2"
  checkout feature3
  merge main
  checkout develop
  merge main
  checkout main
  cherry-pick id: "feature3"
```
