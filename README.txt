https://spaces.redhat.com/display/amqbroker/Using+Brew+images+on+external+clusters+deployed+on+AWS

apiVersion: config.openshift.io/v1
kind: ImageDigestMirrorSet
metadata:
 name: brew-registry-v2
spec:
 imageDigestMirrors:
   - source: registry.redhat.io
     mirrors:
       - brew.registry.redhat.io
   - source: registry.stage.redhat.io
     mirrors:
       - brew.registry.redhat.io
   - source: registry-proxy.engineering.redhat.com
     mirrors:
       - brew.registry.redhat.io


curl --negotiate -u : -X POST -H 'Content-Type: application/json'          \
      --data '{"description":"(describe what the token will be used for)"}' \
      https://employee-token-manager.registry.redhat.com/v1/tokens -s | jq

 https://spaces.redhat.com/display/GITOPS/Install+GitOps+Operator+in+Disconnected+Cluster
