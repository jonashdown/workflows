# Feature branches without tagging

Feature branches are merged to the main branch, when this is done a snapshot can be deployed to lower level environments for testing, and released once testing is complete.

```mermaid
gitGraph
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
  checkout main
  merge feature1
  commit
  branch feature3
  commit
  commit
  checkout feature2
  merge main
  commit
  commit
  checkout feature3
  commit
  checkout main
  merge feature3
  checkout feature2
  merge main
  commit
  commit
  commit
  checkout main
  merge feature2

```