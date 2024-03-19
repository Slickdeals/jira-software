# Jira Software

This repo is responsible for creating the Atlassian Jira Docker image for our internal use.

There's not a lot going on in repo itself other than defining a Dockerfile and a few GitHub Actions.

## Usage
To build an image for Jira Software, simply trigger a new run of the default pipeline for this repo via the [GitLab UI](https://it-gitlab.slickdeals.dev/itops/jira-software/-/pipelines)

The image will be built from the Dockerfile in the `app` folder of this repo. There are two images that will be built from these pipelines, an image for use with our Dev environment, and an image for our Production Jira instance.

Once built, the Docker Image will be tagged with the Git Commit SHA and the version of Jira Software that was used to build the image.

The resulting image will be pushed to the Slickdeals GHCR for use on our systems.
