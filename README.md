# Getting Started :octopus:

Welcome to GERP! We hope you love this tool as much as we do. Refer to the [gerp repo](https://github.com/gerp-project/gerp) for more documentation.

## Copy Template Repo :page_facing_up:

This repo is a template, and you can duplicate it to get a quick and easy setup. Hit the `Use this template` at the top.

## Configuration :wrench:

After duplicating, add the following [secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository) to your repository then you're good to go :smiley:.

```
required secrets:
  PAT

// Your PAT will need the following permissions depending on your target repos and desired templates
repo.public_repo   // Required to make PRs against target repos
repo               // Only needed if you are synchronizing priviate repos
workflow           // Only needed if you are synchronizing anything in the .github directory 
```
To add a target repo, just add it to your [gerp config](.gerp/config.json)

Files placed in the [/template](/template) directory will be synced into the root of target directories. Variables can be substituted using [mustache](http://mustache.github.io/) templating, with inputs provided in your [gerp config](.gerp/config.json). Inputs from your gerp config are applied on a per-repo basis to all files being synced.

## Terms :books:

Template Repo: The source of truth repository that GERP will use to determine which files to sync

Target Repo: A repository that GERP will open pull pull requests against in order to reconcile its files based on the template repository
