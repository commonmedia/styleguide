# Using git

## Git Commit Messages

* If the commit involves migrations, precede the commit message with `(M)`
* End each commit with a reference to the ticket number, if applicable, in the format `refs #5555`
* Keep Gem updates in separate commits
* For Gem update commits, the commit message format is:

```
gem update:

[gem-name] to [version]
[gem-name] to [version]
```

## Git Branch Usage

This assumes the repository has a `staging` branch, which was created off the `master` branch.

1. Create a new branch for your feature, off of the `master` branch. Ideally, this branch name would follow a `name-ticketnumber` format, like `slider-navigation-4856`
2. Develop new features/fixes in this new `name-ticketnumber` branch
3. When you need your feature on staging, checkout the `staging` branch, and merge in your `name-ticketnumber` branch
4. Deploy the `staging` branch to the staging server (typically with `cap staging deploy`)
5. Test your feature/fix
6. If you need to make more changes to your feature/fix, checkout your `name-ticketnumber` branch to make those changes - Any necessary changes/fixes are made on their respective branches (not on `staging` or `master` branchces)
7. Repeat steps 3-6,  until your feature/fix is ready for production
8. If everything is approved, checkout the `master` branch, and merge in your `name-ticketnumber` branch (If the entirety of the `staging` branch is deployable, then you can merge in that branch instead)
9. Deploy `master` branch to production server (typically with `cap production deploy`)

## Core Ideals

* No edits are done on the `master` branch itself
* Each feature/fix has its own branch
* One feature/fix can never hold up the deployment of another feature/fix
