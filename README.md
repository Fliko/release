# Release
This is an example of my proposed release cycle.

## Workflows
### Check Branch Name
Check branch name makes sure any branch merged into staging is like EX-111_branch_description
the first part being your jira ticket EX-111

### Create Release
Creates a github release to be deployed with generated changelog.

### Rebase on Release
As code moves through stages it collects minor changes, this merges codes final form back into dev stages.

## Developer Flow

 - Write code in PRs only
 - Test in develop Branch
 - When Jira ticket moved to review, automatically create pr in staging with webhook
 - At end of Sprint choose branches to be included in next release
 - Merge and delete those branches into staging
 - Manually create release with `DEBUG=release-it:* release-it patch --preRelease=staging --no-npm --github.release=true`
   - make sure changelog is in a form where we have a list of features to test before release is created
 - Make sure all items in RC are tested by end of next sprint
 - Merge RC tag into Main to create official release
 - Deploy to prod
 
## Release Timeline

Sprint (2 weeks) --> RC Created (1hr - 1day) --> RC Tested (2 weeks) --> Create Release and Deploy (1hr - 1day)

Total planned time: 4 weeks + 2 days per release
 
 ## TODO
 
 - Add jira [webhook](https://developer.atlassian.com/server/jira/platform/webhooks/) and jira [workflow](https://github.com/parkhub/save-repo-for-jira-action/blob/master/index.js) for tracking branches 
 - Setup Template for changelog
 - Would be nice if release changelog = pre-release changelog + changes during testing
 
Changelog goal is something like so:

![changelog](/Screenshot%20from%202022-09-21%2007-53-02.png)
