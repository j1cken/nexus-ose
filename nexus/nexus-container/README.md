```
oc new-project ci
oc new-app -n ci https://github.com/j1cken/nexus-ose.git --context-dir=nexus/nexus-container --strategy=docker --name=nexus --docker-image="registry.access.redhat.com/rhel:latest"
oc expose svc nexus -n ci --hostname=nexus.192.168.122.109.xip.io
```
