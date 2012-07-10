# Using git

## Git Branch Usage

1. Create `staging-YYYYMMDD` branch
1. Pull current `master` branch into `staging` branch
1. Develop new features/fixes in a new branch that's specific to that feature/fix … Ideally, these branch names would follow a `feature/fix-name-ticketnumber` format, like `gourmet-stores-page-5538`
1. Pull from any branches that need to be tested into the `staging-YYYYMMDD` branch
1. Deploy `staging-YYYYMMDD` branch to staging server
1. Test
1. Any necessary changes/fixes for customer approval are made on their respective branches, then pulled back into the `staging-YYYYMMDD` branch
1. If everything is approved, pull `staging-YYYYMMDD` branch into `master` branch … If only one or some features are approved, pull their respective branches into `master` branch
1. Deploy `master` branch to production server
1. ...repeat as necessary

## Core Ideals

* No edits are done on the `master` branch itself
* Each feature/fix has its own branch
* One feature/fix can never hold up the deployment of another feature/fix 
* The `staging` branch is disposable