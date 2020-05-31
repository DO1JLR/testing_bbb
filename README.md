 testing bbb server stuff
=========================

This ansible playbook is **only** designed to set up a bbb server for **TESTING**!
This means, we do not encrypt any secret variables via ansible-vault.

As playbook we use the ``site.yml`` playbook.

To use this role by yourself, you have to edit the fqdn host in the host.ini file and make sure, you can access it via root ssh.


 What is this playbook doing?
---------------------
1. We install some base-packages.
2. We add do1jlr's SSH Keys
3. We install bigbluebutton

 some hints
-----------
To check out this repo properly checkout the submodules!
```
git pull origin master
git submodule update --init --recursive
git config --global submodule.recurse true
```

You can install ansible by executing ``sudo make install``.
