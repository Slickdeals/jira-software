# Jira Software

This repo is responsible for creating the Atlassian Jira Docker images for our internal use that has been customized with a MySQL ODBC Connector.

There's not a lot going on in repo itself other than defining a Dockerfile and a few GitHub Actions.

## Usage
To trigger a build of the Dev Jira Docker Image, make your changes in a branch and open a PR against the develop branch. Check the status of [GH Action](https://github.com/Slickdeals/jira-software/actions/workflows/build-dev-image.yml) and view the output of the job run for your changes.

Once you are happy with your changes, merge your PR into the develop branch. This will trigger a build of the Dev Jira Docker Image and push it to the Slickdeals GHCR.

Merging your changes against the develop branch will trigger a Push of the Dev Jira Docker Image to the Slickdeals GHCR.

Once changes have been tested against the develop branch, they can be merged into the main branch. This will trigger a build of the Production Jira Docker Image and push it to the Slickdeals GHCR.
