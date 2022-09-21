# Getting Started
Welcome to GERP! We hope you love this tool as much as we do :)

## Copy Template Repo 📄
This repo is a template, and you can duplicate it to get a quick and easy setup, just supply the following secrets after you use the template!
```
required secrets:
  PAT

// Your PAT will need the following permissions depending on your target repos and desired templates
repo.public_repo   // Required to make PRs against target repos
repo               // Only needed if you are synchronizing priviate repos
workflow           // Only needed if you are synchronizing anything in the .github directory 
```

## Configuration ⚙️
Files placed in the [/template](/template) directory will be synced into the root of target directories.

Variables can be substituted using [mustache](http://mustache.github.io/) templating, with values provided in your [gerp config](.gerp/config.json)

Variables from your gerp config are applied on a per-repo basis to all files being synced.


## Terms 📖
Template Repo : The source of truth repository that GERP will use to determine which files to sync
Target Repo   : A repository that GERP will open pull pull requests against in order to reconcile its files based on the template repository
