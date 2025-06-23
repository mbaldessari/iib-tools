# Instructions

Run it like this:

```sh
OPERATOR=kernel-module-management \
INDEX_IMAGES=registry-proxy.engineering.redhat.com/rh-osbs/iib:993390 \
CHANNELS=release-2.4 make iib
```

A mirroring config will be needed:

```yaml
apiVersion: operator.openshift.io/v1alpha1
kind: ImageContentSourcePolicy
metadata:
  name: kmm-stage
spec:
  repositoryDigestMirrors:
  - mirrors:
    - registry.stage.redhat.io
    source: registry.redhat.io/kmm
```
