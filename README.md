Hastebin server on OpenShift
============================

OpenShift deployment for [haste-server](https://github.com/seejohnrun/haste-server).

Cartridge Dependencies
----------------------
* [nodejs](https://developers.openshift.com/en/node-js-overview.html)
* [redis](https://github.com/smarterclayton/openshift-redis-cart)

Quick deploy command
--------------------
```sh
rhc app create --scaling hastebin \
  nodejs-0.10 \
  "http://cartreflect-claytondev.rhcloud.com/reflect?github=smarterclayton/openshift-redis-cart" \
  --from-code git://github.com/abn/haste-server-openshift.git
```

Configuration
-------------
#### _*.hasterc*_
This file contains configuration for haste-server repository to use along with the branch and is sourced in the action hooks.

####_*.configure*_
This python script allows you to modify both the _config.js_ and _package.json_ files used by haste. This is run both pre-build and pre-start as part of _.update_.
