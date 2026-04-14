
## Copier

This repository provides a [copier](https://copier.readthedocs.io/en/stable/)
template for creating lightweight, language‑specific project skeletons. It
offers a consistent and reproducible starting point across projects and makes
it easy to apply improvements when the template is updated.


### Prerequisites

Install the Copier command:
* **Quick option:** `uv tool install copier`
* **Documentation:** https://copier.readthedocs.io/en/stable


#### Default Config

User-specific values are loaded from the global configuration file - 
`~/.config/copier/settings.yml`. If the file is not present or not saved, empty
strings are used as defaults.
```
defaults:
  author_name : "Karsh"
  author_email: "karshMail@iCloud.com"
  github_user : "karshPrime"
```

### Create New Project

Run the following command:

```bash
$ copier copy git@github.com:karshPrime/template-generic path/to/project --trust
```
Answer the Copier prompts to configure the project.
* **Project Description:** Optional plain‑text description of the project.
* **Language extension:** Choose the file extension or language identifier for
  the template (for example `py`, `js`, `ts`, `go`, `rs`). The template will use
  this value to create example source files and set up basic filenames.

**Note:** The `--trust` option is required because the template runs `uv` and
`git` commands.


## Template Readme

This project uses [template/README.md.jinja](template/README.md.jinja) as the
main README file, which is copied into the generated project.

The `.jinja` file automatically inserts the project name and description based
on the answers provided during copier copy.

