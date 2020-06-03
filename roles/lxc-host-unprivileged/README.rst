This role sets up unprivileged containers with plain LXC.

This roles is tested on Debian stable and, of course, developed
according to my personal preferences (e.g., with *one* user and *one*
network per container for a high degree of isolation).

In order to manage complexity, this role has limited flexibility/
configuration options.

Developing and using this role which builds on plain LXC instead of
using, e.g., LXD is motivated by
`the concerns about running the snap-provided LXD <https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=768073>`__
and the slight bloat of LXD in general (e.g., if you do not need
``lxcfs`` or if you do not want to run a cluster).

This role will not

* configure anything inside the containers;
* configure the network (i.e., the host's ``iptables``) for the
  containers.
