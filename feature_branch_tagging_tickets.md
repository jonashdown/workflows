# Feature branches and tagging

Feature branches are merged to the main branch, when this is done a git tag is created. this tag can be deployed to lower level environments for testing, and released once testing is complete.

```mermaid
gitGraph
  commit
  checkout main
  commit
  branch feature1
  commit
  checkout main
  merge feature1
  commit id: "feature1" tag: "1.0.0"
  commit
  checkout main
  branch feature2
  branch ticket1
  commit
  checkout feature2
  merge ticket1
  branch ticket2
  commit
  checkout feature2
  merge ticket2
  branch ticket3
  commit
  checkout feature2
  merge ticket3
  branch ticket4
  commit
  checkout feature2
  merge ticket4
  checkout main
  commit
  branch feature3
  branch ticket7
  commit
  checkout feature3
  merge ticket7
  checkout feature2
  commit
  commit
  checkout feature3
  commit
  checkout main
  merge feature3
  commit id:"feature3" tag: "1.0.1"
  checkout feature2
  merge main
  commit
  commit
  commit
  checkout main
  merge feature2
  commit id:"feature2" tag: "1.0.2"

```