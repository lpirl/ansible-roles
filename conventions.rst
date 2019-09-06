Basically, a note to myself: :)

general
=======

* do not use abbreviated YAML syntax

  * e.g., not: ``[foo, bar]``, ``package: name=foo state=present``

how to modify configurations
============================

* try to preserve the possibility to have local modifications
  (done manually on remote machine)
* try to make it transparent which files have been edited via Ansible

* if we can add our changes to a separate file
  (in directories like ``/etc/cron.d``)

  * prefer writing the file via ``blockinfile``

    * since it creates nice "managed by Ansible" markers by itself
    * instead of using the ``copy`` module
    * load contents with, e.g., ``{{ lookup('file', '/foo.txt') }}``
    * # let's see if this is feasible

* if we *cannot* add our changes to a separate file
  (e.g. ``/etc/postfix/main.cf``)

  * prefer ``lineinfile``

    * since it can deal with pre-existing configurations
      (i.e., lines in the file)

task scheduling
===============

* try to use systemd timers

  * profit from useful features

    * e.g., ``ConditionCapability``, ``Persistent``

  * it'll probably go in that direction anyway

* to defer tasks on battery, a separate, unified solution is required

  * i.e., do not include a solution to wait for AC in every timer/unit
    separately

    * since most systems do have permanent AC and it would be a waste
      of resources to run the checks anyway

  * maybe systemd override files which add ``ExecStartPre`` to wait
    for AC
