 testing bbb server stuff
=========================

This ansible playbook is **only** designed to set up a bbb server for **TESTING**!
This means, we do not encrypt any secret variables via ansible-vault.

As playbook we use the ``site.yml`` playbook.

To use this role by yourself, you have to edit the fqdn host in the host.ini file and make sure, you can access it via root ssh.


For a overview which server we are using, **have a look into hosts.ini!**
For the exact commit of the roles we are using please have a look at git submodules and the roles folder!


 What is this playbook doing?
---------------------
1. We install some base-packages.
2. We add do1jlr's and 0boro's SSH Keys
3. We install bigbluebutton
4. We install differen scalelite versions
5. We install node-exporter (public, no passwort, no TLS) for optional monitoring
6. We try to connect everything (missing)


 some hints
-----------
To check out this repo properly checkout the submodules!
```
git pull origin master
git submodule update --init --recursive
git config --global submodule.recurse true
```

You can install ansible by executing ``sudo make install``.
