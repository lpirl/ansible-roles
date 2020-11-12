some Ansible roles
==================

This repository contains Ansible roles.

The roles cover most of my administrative tasks and configurations
(which have to be fulfilled/applied more than once).

The roles are developed mainly for Debian(-based) systems. The stable
and oldstable releases should work. Ubuntu might also work or, at
least, almost work. Other distributions probably won't work.

The roles are intended to be somewhat reusable,
but please do not apply them blindly.
Make sure you read and understand a role before running it.
Otherwise, you'll possibly loose something you love.

If you *do* run this roles, have recent backups.

Feel free to read/try/use/extend them
and to contact me if you have any questions.

The most intensively developed, used and maintained role is
``managed_host``.
You (should) find README files in the roles' directories.
There are also
`a few random notes on (intended) conventions <conventions.rst>`__.

Configuration files which are not used by these roles but maybe
interesting for others as well are kept in
`this repository <https://gitlab.com/lpirl/dotfiles>`__.
