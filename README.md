Workers.coop Documentation
==========================

This repo contains the files that are used to build the live site at
[docs.workers.coop](https://docs.workers.coop/) and staging site at
[stage.docs.workers.coop](https://stage.docs.workers.coop/).

How it works
------------

When changes are committed to this repo the site is built in a Docker
container, checked using
[pymarkdown](https://github.com/jackdewinter/pymarkdown) and
[yamllint](https://github.com/adrienverge/yamllint) and if there are not errors
the site is then rsync'ed to the `stage.docs.workers.coop` site, the live
`docs.workers.coop` site update needs [a manual click in the GitLab CI
interface](https://git.coop/workers/docs/-/pipelines) &mdash; please check your
changes on the staging site before updating the live site!

You can use the GitLab editor at `git.coop` and the `stage.docs.workers.coop`
site when working on this documentation or you can checkoit and host the site
locally by installing MkDocs and starting a local web server:

```bash
pipx install mkdocs
git clone git@git.coop:workers/docs.git
cd docs
mkdocs serve
```

MkDocs
------

See the MkDocs [getting started](https://www.mkdocs.org/getting-started/) and
the [writing your docs](https://www.mkdocs.org/user-guide/writing-your-docs/)
guides for more information.

Linting
-------

You can enable the linting of YAML and Markdown files prior to changes being
committed by installing [pre-commit](https://pre-commit.com/) locally and for
this repo, for example:

```bash
pipx install pre-commit
git clone git@git.coop:workers/docs.git
cd docs
pre-commit install
```

You can also install the linting packages locally and manually check the files,
for example:

```bash
pipx install pymarkdown
pipx install yamllint
git clone git@git.coop:workers/docs.git
cd docs
yamllint .
pymarkdown scan .
```

Project Access
--------------

If you have an account at `git.coop` you can request access to [this
project](https://git.coop/workers/docs), if don't have an account you can clone
the [GitHub mirror](https://github.com/workers-coop/docs) and create a pull
request there and then somone who does have access can apply a patch file on
your behalf.
