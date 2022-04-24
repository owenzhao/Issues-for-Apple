# Xcode Couldn't Add Forked Repo if the Original Repo Was Added First in SPM

## Issue
If you added a repo in SPM, then for some reason, you had to fork the repo. When you replaced the repo to your forked repo. Xcode wouldn't work. Xcode would still remember the old the repo, then couldn't find the new version of forked repo.

A workaround was to manually removed the cached repo in Xcode by right click. Then added the forked repo.

## Steps
1. Create a SwiftUI project.
2. Add a Swift Package in SPM. Say: "git@github.com:AppPear/ChartView.git", choose version: 1.5.5 ..< 2.0.0
3. Build the project.
4. Fork the repo. Edit something and upload the new version as 1.5.7.
5. Remove the old package. Add the forked repo. Say: "git@github.com:owenzhao/ChartView.git", choose version: 1.5.7 ..< 2.0.0.

### Expected
Xcode get the new forked package.

### Happened
Xcode failed at dependencies check.