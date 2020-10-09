RHSat-Install
===========

This role will install satellite, and do initial day 0 configuration, including (by default) configuring RHEL 7 + Satellite Activation Key
and the minimal upstream requirements for that, eg. a Composite Content View, Repositories, Host Group, etc, and the downstream configuration
items as well: Activation Key and Hostgroup.

Users of this role can configure additional CVs, CCVs, AKs, HGs, or even rebuild the provided configurations.

Requirements
------------

Ansible 2.8 or higher

Red Hat Enterprise Linux 7 or equivalent

Valid Red Hat Subscriptions

Role Variables
--------------

See inline comments in `defaults/main.yml` for details.


Significant Tags
----------------

This full playbook can take a long time to run, and especially during development, it is helpful to limit what is executed.
In order (though they are intertwinded in reality): serverprep, satinstall, satcerts, satconfigure, satcontent, satcontentsync.

Dependencies
------------

Example Playbooks
-----------------

License
-------

[GPLv3](LICENSE)

Author Information
------------------
Ron Sawyer <rsawyer@redhat.com>    
Cory McKee <cmckee@redhat.com>    
Greg Hellings <ghelling@redhat.com>    
Jeff Warnica <jwarnica@redhat.com>    
