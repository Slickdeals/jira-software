# Jira Software

This repo is responsible for creating the Jira Software image used for our on-prem Jira servers.

There's not a lot going on in repo itself other than defining a Dockerfile and gitlab-ci.yml file for the CI/CD pipeline.

## Usage
To build an image for Jira Software, simply trigger a new run of the default pipeline for this repo via the [GitLab UI](https://it-gitlab.slickdeals.dev/itops/jira-software/-/pipelines)

Set a variable `DEFAULT_RELEASE_TAG` to configure the image version to build. 

Ensure you only use semVer format for the `DEFAULT_RELEASE_TAG` variable, or simply leave it unset to run a build against whatever image is currently present at the `latest` tag from the [upstream Docker Hub repo](https://hub.docker.com/r/atlassian/jira-software/tags?page=1&name=latest)


The resulting new image will be automatically saved into this Project's [Container Registry](https://it-gitlab.slickdeals.dev/itops/jira-software/container_registry) and should be pullable with Docker CLI from there.
