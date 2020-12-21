# p6m7g8 - Productivity


## Getting Started

- p6m7g8/p6dfz: bin/bootstrap.zsh - Installation
- p6m7g8: this README
- p6m7g8.github.io: MKDocs site

## Layout

- p6df-foo: Shell glue files
- p6-foo: Application
- p6foo: Library

## Modules

### Shell Glue

- p6df-R
- p6df-aws
- p6df-awscdk
- p6df-awscdk8s
- p6df-awscdktf
- p6df-azure
- p6df-bash
- p6df-core
- p6df-darwin
- p6df-dev
- p6df-docker
- p6df-emacs
- p6df-gcp
- p6df-git
- p6df-github
- p6df-go
- p6df-helm
- p6df-homebrew
- p6df-irc
- p6df-java
- p6df-jc
- p6df-jenkins
- p6df-jira
- p6df-kubernetes
- p6df-lua
- p6df-macosx
- p6df-mysql
- p6df-node
- p6df-oci
- p6df-openssl
- p6df-oracle
- p6df-perl
- p6df-pgsql
- p6df-projen
- p6df-python
- p6df-ruby
- p6df-scala
- p6df-security
- p6df-shell
- p6df-slack
- p6df-sqlite
- p6df-sqlserver
- p6df-sudo
- p6df-svn
- p6df-terraform
- p6df-vim
- p6df-vscode
- p6df-zsh

### Applications

- p6-account-vending-machine
- p6-aws-eks-cluster
- p6-barrier
- p6-barrier-app
- p6-cdk8s-hello-world
- p6-cdktf-hello-world
- p6-cirrus-inc
- p6-docs
- p6-go-hello-world
- p6-namer
- p6-namer-app

### Libraries

- p6aws
- p6awscdk
- p6cicd
- p6common
- p6emacs
- p6git
- p6github
- p6helm
- p6jenkins
- p6kubernetes
- p6macosx
- p6openssl
- p6perl
- p6shell
- p6svn
- p6test
- p6types

## Design

`~/.zshrc` runs and hooks `~/.zsh-me` (_Eventually bash too_)
which then recursively loads the modules and calls ::init()

You then need to run ::brew() and ::langs() which is what differentiates us
from all other frameworks that assume you have the dependencies pre-installed.

## API (a module or library)

- ::version()
- ::init()
- ::deps()
