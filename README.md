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

## Developer Flow

 - Write code in PRs only
 - Test in develop Branch
 - [Not Implemented] On Jira ticket moved to review, create staging pr
 - At end of Sprint choose branches to be included in next release
 - Merge and delete those branches into staging
 - Manually create release with `DEBUG=release-it:* release-it patch --preRelease=staging --no-npm --github.release=true`
 - Make sure all items in RC are tested by end of next sprint
 - Merge RC tag into Main to create official release
 - Deploy to prod