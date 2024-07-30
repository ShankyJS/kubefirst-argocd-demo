# ArgoCD with Kubefirst demo

[![en](https://img.shields.io/badge/lang-en-red.svg)](./README.md)
[![es](https://img.shields.io/badge/lang-es-yellow.svg)](./README-es.md)


[Kubefirst](https://kubefirst.io/) delivers instant GitOps platforms so you can have the most popular open source platform tools working together in minutes. 🚀.

![Kubefirst k3d architecture](image.png)

## Installation

Install it with Homebrew (MacOS) follow the [documentation](https://docs.kubefirst.io/k3d/quick-start/install) to install in different OS.

```bash
brew install kubefirst/tools/kubefirst
brew install mkcert
mkcert -install
```

## What is K3d?

k3d is a lightweight wrapper to run k3s (Rancher Lab's minimal Kubernetes distribution) in docker. k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes

## Creating our K3d environment

In order to create our K3d environment there are some prerequisites

1. Docker should be installed and up and running.
2. A Github account with a GITHUB_TOKEN exposed as an env var in our shell.

Then we can run the following

```bash
kubefirst k3d create
```

## Login credentials

If you need the credentials to log in to any of the internal systems run the following command:

```bash
kubefirst k3d root-credentials


  ----------------------------------------------------------------------
  k3d Authentication

  Keep this data secure. These passwords can be used to access the
  following applications in your platform.
  ----------------------------------------------------------------------

  Argo CD admin Password: password

  KBot User Password: random

  Vault root Token: randomtoken
```
