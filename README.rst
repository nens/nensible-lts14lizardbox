N&S LTS 14.04 lizard base box
=============================

All the common requirements of a regular lizard4/5 site on an ubuntu 14.04 LTS
base. "Regular lizard4/5" means a modern django 1.6+ that is OK with the gdal
and mapnik dependencies as provided by the LTS. The goal is not to litter the
base box with PPAs and custom packages.

If a real variant with for instance a really fresh gdal is needed: make it an
explicit choice and install a self-build gdal package. So: later on, an
if/else can be added. But don't make too many of them. If the role starts to
become unmanageable: apparently you've done something to the role that's not
its goal!


What does the role mean?
------------------------

If a server has this role, it is a pretty standard common-at-N&S box. You
could put lizard5 or a modernized lizard4 site or TRS on it. The kind of
configuration you'd use to run jenkins on: lizard-map and trs and
lizard-security should be able to run ``bin/test`` on them (apart from
additionally needing to install jenkins and a database server).

In the case of a jenkins box, you'd might have to install some extra packages.

In any case, it isn't a wildly modified "PPA-invested" box.


Requirements
------------

It is build upon ubuntu's 14.04 LTS release. When a new LTS comes out it is
probably a good time to make a new one specifically for that LTS: a nice
cleanup instead of bolting "if/else" statements onto this role.


Example playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too::

    - hosts: servers
      roles:
         - nensible-lts14lizardbox


License
-------

BSD


Author Information
------------------

Created by `Reinout van Rees <http://reinout.vanrees.org>`_ at `Nelen &
Schuurmans <http://www.nelen-schuurmans.nl>`_.
