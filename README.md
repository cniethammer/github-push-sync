# github-to-gitlab-push-sync
This workflow sets up a GitHub action that will sync branches/tags from a GitHub repository to a gitlab repository.

To set this up:

1.) Create the target repository on the gitlab server and push the initial version of the repo manually.

2.) Create a project access token for the repository on the gitlab server.  (Project->Settings->Access Tokens->Add new token)
    The token needs the write_repository scope and maintainer role.

3.) Create action secrets on the GitHub repository named ACCESS_TOKEN_NAME and ACCESS_TOKEN with the
    corresponding values. (Settings->Secrets and Variables->Actions->New repository secret)

4.) Add the .github/workflow/github-to-gitlab-push-sync.yml file to your GitHub repository.
