module
  RUNTIME common
  overrides

common
  bin
	install
	init
	prereq
	config
	deps
	proxy
	tag
	bump_version
  conf
	defaults.conf
  json
  yml
  lib
	sh
	perl
	python
  libexec
  tests

pgollucci/home
  *.!z


pgollucci/p6zsh
	bin/
		h*
	.zshrc
		local DEBUG=1
		local DISABLE_ENVS=
		ZDOTDIR=$HOME
		ZSH_DIR=$ZDOTDIR/.zsh

		set theme

		bootstrap

		load
			frameworks [zplug, zpresto, oh-my-zsh]
			theme
			  ALL config here
			modules
			local
			prompts
			completions
			completions_local

	.z*

pgollucci/p6util-bridge

pgollucci/p6util-sh
pgollucci/p6util-perl
pgollucci/p6util-python

pgollucci/p6h-aws/
	DEPENDS pgollucci/p6util-sh
	RUNTIME pgollucci/cirrus*

  alias sts=cirrus_something

  bin
  conf
  lib

pgollucci/cirrus-bootstrap
pgollucci/cirrus-dev
pgollucci/cirrus-core
  bin
  conf
  lib
	cfg
	shorts
	api
	uw
pgollucci/cirrus-user-iam
  RUNTIME pgollucci/daas
pgollucci/cirrus-user-sts
  RUNTIME pgollucci/daas
pgollucci/cirrus-user-organizations
  RUNTIME pgollucci/daas
pgollucci/cirrus-stacks
  yml

pgollucci/daas-jc
pgollucci/daas-ping
pgollucci/daas-adfs

pgollucci/cumulus
  RUMTIEM cicd-*, orch-*, daas-*, cirrus-user-*
  give me aws infra [accounts, networking, apps]

pgollucci/cicd-jenkins
pgollucci/cicd-github
pgollucci/orch-chef
pgollucci/orch-drone
