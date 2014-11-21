Hastebin server on OpenShift
============================

OpenShift deployment for haste-server (http://hastebin.com/)

Cartridge Dependencies
----------------------
* [nodejs](https://developers.openshift.com/en/node-js-overview.html)
* [redis](https://github.com/smarterclayton/openshift-redis-cart)

Quick deploy command
--------------------
```sh
itos app create --scaling hastebintest \
  nodejs-0.10 \
  "http://cartreflect-claytondev.rhcloud.com/reflect?github=smarterclayton/openshift-redis-cart" \
  --from-code git://github.com/abn/haste-server-openshift.git
```
