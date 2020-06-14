 testing bbb server stuff
=========================

This ansible playbook is **only** designed to set up a bbb server for **TESTING**!
This means, we do not encrypt any secret variables via ansible-vault.
But that also means you can use this playbook yourself and reproduce the installation here on your own.
Since this playbook and the configuration is partly adapted to your own domains and the same, here are the **things you should change to test the playbook yourself:**
 + replace the server in the ``hosts.ini`` server with your own servers and give them a fqdn-Domain Name.
   + For scalelite we use ``Debian 10`` as operating system
   + For bbb we use ``Ubuntu 16.04`` as operating system
 + replace the hostnames we created for our hosts with the hosts you are using.
 + ***(optionally)*** change the paybook part where we add our own ssh keys.

 OVERVIEW
--------------

As playbook we use the ``site.yml`` playbook.

For the exact commit of the roles we are using please have a look at git submodules and the roles folder!

For any trouble or questions please feel welcome to create an issue or a pull-request!

 What is this playbook doing?
---------------------
1. We install some base-packages.
2. We add do1jlr's and 0boro's SSH Keys
3. We install some bigbluebutton severs *(scalelite require at least 3 servers)*
4. We install differen scalelite versions
5. We install node-exporter (public, no passwort, no TLS) for optional monitoring
  * We won't install bigbluebutton-exporter, because it is not public code.
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

You can see scalelite secrets with:
```
ansible scalelite -m setup -a "filter=ansible_local"
```
