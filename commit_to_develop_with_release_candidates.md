# Commit to Develop with Release Candidates


Code changes are commited directly to the develop branch, release candidates are cherry-picked into releasde candidate branches that track the main branch and delpoyed to lower level environments. Releases are made when release-candidates are merged

```mermaid
gitGraph
  commit
  branch develop
  commit
  commit id: "Feature 1"
  commit
  checkout main
  commit
  commit
  branch rc-1
  commit tag:"rc:1.0.0"
  cherry-pick id: "Feature 1"
  checkout develop
  commit
  commit id: "Feature 2"
  commit
  commit id: "Feature 3"
  checkout main
  commit
  branch rc-2
  cherry-pick id: "Feature 3"
  commit tag:"rc-2.0.0"
  checkout develop
  commit
  commit
  commit
  checkout rc-1
  cherry-pick id: "Feature 2"
  checkout main
  merge rc-1
  commit tag:"1.0.0"
  checkout develop
  merge main
  commit id: "Feature 4"
  checkout rc-2
  merge main
  cherry-pick id:"Feature 4"
  commit tag:"rc-2.0.1"
  checkout main
  merge rc-2
  commit tag:"2.0.1"
```