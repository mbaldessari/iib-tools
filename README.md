Run it like this:

```sh
OPERATOR=kernel-module-management INDEX_IMAGES=registry-proxy.engineering.redhat.com/rh-osbs/iib:993390 CHANNELS=release-2.4 make iib
```


Bunch of ideas from:
https://spaces.redhat.com/display/amqbroker/Using+Brew+images+on+external+clusters+deployed+on+AWS

https://spaces.redhat.com/display/GITOPS/Install+GitOps+Operator+in+Disconnected+Cluster

apiVersion: operator.openshift.io/v1alpha1
kind: ImageContentSourcePolicy
metadata:
  name: kmm-stage
spec:
  repositoryDigestMirrors:
  - mirrors:
    - registry.stage.redhat.io
    source: registry.redhat.io/kmm
