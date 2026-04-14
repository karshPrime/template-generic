
## Copier

This repository provides a [copier](https://copier.readthedocs.io/en/stable/)
template for creating lightweight, language‑specific project skeletons. It
offers a consistent and reproducible starting point across projects and makes
it easy to apply improvements when the template is updated.


### Prerequisites

Install the Copier command:
* **Quick option:** `uv tool install copier`
* **Documentation:** https://copier.readthedocs.io/en/stable


### Create New Project

Run the following command:

```bash
$ copier copy git@github.com:karshPrime/template-generic path/to/project.xx --trust
```
* Replace the `.xx` extension with the language of the new project.
* **Project Description:** Answer the Copier prompt with an optional
  plain‑text description of your project.
* The `--trust` option is required because the template runs `uv` and `git`
  commands.


### Default Config

User-specific values are loaded from the global configuration file - 
`~/.config/copier/settings.yml`. If the file is not present or not saved, empty
strings are used as defaults.
```
defaults:
  author_name : "Karsh"
  author_email: "karshMail@iCloud.com"
  github_user : "karshPrime"
```

## Template Readme

This project uses [template/README.md.jinja](template/README.md.jinja) as the
main README file, which is copied into the generated project.

The `.jinja` file automatically inserts the project name and description based
on the answers provided during copier copy.

