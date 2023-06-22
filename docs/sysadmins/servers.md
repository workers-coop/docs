Servers
=======

The `workers.coop` servers are managed using Ansible and the code for this is
hosted in the [servers repo](https://git.coop/workers/servers).

auth.workers.coop
-----------------

The [auth.workers.coop](https://auth.workers.coop/) server is running
[Authentik](https://goauthentik.io/) in a Docker container to provide SSO for
other services.

cal.workers.coop
----------------

The [conversations.workers.coop](https://conversations.workers.coop/) server,
`cal.workers.coop`, is running [Cal.com](https://github.com/calcom/cal.com/)
installed using the [Docker repo](https://github.com/calcom/docker) using the
`conversations` account on the server and an Apache reverse proxy.

chat.workers.coop
-----------------

The [chat.workers.coop](https://chat.workers.coop/) server provIdes a Matrix
service with a Synapse back-end and a Element front end.

forum.workers.coop
------------------

The [forum.workers.coop](https://forum.workers.coop/) server is running
[Discourse](https://discourse.org/) in a Docker container, wit the host
providing an incomming and outgoing SMTP service configured using [this Ansible
role](https://git.coop/webarch/discourse).

office.workers.coop
-------------------

The [office.workers.coop](https://office.workers.coop/) server is running:

* WordPress / CiviCRM on the `wp` account.
* Nextcloud on the `cloud` account.
* ONLYOFFICE.
* Kimai.
