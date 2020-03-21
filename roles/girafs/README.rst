Installs `girafs <https://gitlab.com/lpirl/girafs>`__ – a tool for
two-way sync of git clones – in the following way:

* installed under separate user (variable ``girafs_user``)
* installs nginx and installs a configuration to have the girafs Webhook
  listener server reverse-proxied
* installs systemd unit to run/start girafs
* girafs configuration needs to be provided (variable ``girafs_config``)
