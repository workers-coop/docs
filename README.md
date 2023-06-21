# Workers.coop Documentation

This repo contains the files that are used to build the live site at [docs.workers.coop](https://docs.workers.coop/) and staging site at [stage.docs.workers.coop](https://stage.docs.workers.coop/).

When changes are committed to this repo the site is built in a Docker contaier and then rsync'ed to the server hosting the site, the `stage.docs.workers.coop` site is automatically updated with every commit, the live `docs.workers.coop` site update needs [a manual click in the GitLab CI interface](https://git.coop/workers/docs/-/pipelines) &mdash; please check your changes on the staging site before updating the live site!

You can use the GitLab editor at `git.coop` and the `stage.docs.workers.coop` site when working on this documentation or you can checkoit and host the site locally by installing MkDocs and starting a local web server:

```bash
pipx install mkdocs
git clone git@git.coop:workers/docs.git
cd docs
mkdocs serve
```

See the MkDocs [getting started](https://www.mkdocs.org/getting-started/) and the [writing your docs](https://www.mkdocs.org/user-guide/writing-your-docs/) guides for more information.

If you have an account at `git.coop` you can request access to [this project](https://git.coop/workers/docs), if don't have an account you can clone the [GitHub mirror](https://github.com/workers-coop/docs) and create a pull request there and then somone who does have access can apply a patch file on your behalf.

