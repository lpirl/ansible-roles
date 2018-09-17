This repository contains Ansible roles for Debian(-based) systems.

The roles cover most of my administrative tasks and configurations
which have to be fulfilled/applied more than once or twice.

The roles are intended to be somewhat generic and reusable,
but please do not apply them blindly.
Make sure you read and understand a role before running it.
Otherwise, you'll possibly loose something you love.

If you *do* run this roles, have recent backups.

Feel free to read/try/use/extend them
and to contact me if you have any questions.

The most intensively developed, used and maintained role is
``managed_host``. You (should) find README files in the roles'
directories.

For the most part, the roles work by **modifying default configuration
files** of Debian installations **instead of replacing them** with
files or files created from templates. This "design" was required
because the roles were developed for already configured systems with
existing different configurations. Hence, configuration files could not
be replaced, but had to be edited by the roles; ideally without
wracking the other existing configuration symbols.
