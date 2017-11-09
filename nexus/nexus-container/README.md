```
oc import-image openshift/rhel7 --from=registry.access.redhat.com/rhel7/rhel --confirm -n openshift
oc new-project ci
oc new-app -n ci https://github.com/j1cken/nexus-ose.git --context-dir=nexus/nexus-container --strategy=docker --name=nexus --image-stream="openshift/rhel7:latest"
oc expose svc nexus -n ci --hostname=nexus.atmy.openshift.cloud
```
