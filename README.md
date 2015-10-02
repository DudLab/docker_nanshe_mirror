[![](https://badge.imagelayers.io/jakirkham/nanshe:latest.svg)](https://imagelayers.io/?images=jakirkham/nanshe:latest 'Get your own badge on imagelayers.io')

# Purpose

Allows for a lightweight mirroring of the `nanshe` container ( <https://registry.hub.docker.com/u/nanshe/nanshe> ). Thus, codebases pulling from the original `jakirkham/nanshe` image will still pull the same common layers.

# Building

## Automatic

This repo is part of an automated build, which is hosted on Docker Hub ( <https://registry.hub.docker.com/u/jakirkham/nanshe> ). Changes added to this trigger an automatic rebuild and deploy the resulting image to Docker Hub. To download an existing image, one simply needs to run `docker pull jakirkham/nanshe`.

## Manual

If one wishes to develop this repo, building will need to be performed manually. This container can be built simply by `cd`ing into the repo and using `docker build -t <NAME> .` where `<NAME>` is the name tagged to the image built. More information about building can be found in Docker's documentation ( <https://docs.docker.com/reference/builder> ). Please consider opening a pull request for changes that you make.

# Testing

The container used by this container as a base, `nanshe/nanshe`, is tested independently along with its contents. As this image is merely a placeholder for `nanshe/nanshe` and does nothing but use that image, no further testing is performed.

# Usage

Once an image is acquired either from one of the provided builds or manually, the image is designed to provide a preconfigured shell environment. Simply run `docker run -it <NAME>`. This will configure Grid Engine and a number of environment variables useful for maintaining it and starts up `bash`. At that point, any `nanshe` command can be run. In the case of an automated build, `<NAME>` is `jakirkham/nanshe`.
