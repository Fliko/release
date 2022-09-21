# Release
This is an example of my proposed release cycle.

## Workflows
### Check Branch Name
Check branch name makes sure any branch merged into staging is like EX-111_branch_description
the first part being your jira ticket EX-111

### Create Release
Creates a github release to be deployed with generated changelog.

### Rebase on Release
As code moves through stages it collects minor changes, all branches should be up to date with production latest

## Manually Generating RC