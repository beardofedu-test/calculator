## Release branches

When we discussed branching strategies with multiple collaborators, we talked about the GitHub Flow and the Git Flow. You might have noticed on the Git Flow diagram the existence of a `release` branch.

The `release` branch is created as part of a formalized release process that enables you to control if any new changes are merged into it, while still enabling continued development on the `dev` branch. In most instances, the `release` branch is created from the `dev` branch after at least one change has been merged into the `dev` branch.

Once a `release` branch is created, formal testing on the upcoming release can be carried out. With a `release` branch created, the only changes that should be made to the `release` branch should be fixes for bugs found on the `release` branch. New feature development should continue to be taking place on `feature` branches created off of and merged into the `dev` branch.

Once the `release` branch has been finalized and your release is ready you can either create your new release from the release branch and _then_ merge it into the `main` branch or you can merge the `release` branch into the `main` branch and then create (or "cut") the release.

Once the release has been merged into the `main` branch, the `dev` branch should be updated with the latest version of `main` and subsequent `feature` branches should be updated with the latest version of the `dev` branch.

For some amazing images and descriptions of a workflow that utilizes a `release` branch, you should check out this documentation:

- [mobify/branching-strategy](https://github.com/mobify/branching-strategy/blob/master/release-deployment.md)