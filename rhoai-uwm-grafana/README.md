# Grafana

This installs the grafana operator along with an instance of grafana for application monitoring. The base is split into folders, one for the operator and another for the actual grafana instance. If you haven't installed grafana before you need to install the operator first so the CRDs are added before deploying the instance.

These bases cannot be deployed directly into a cluster, a a minimum you will need an overlay that creates a Namespace and an OperatorGroup, see the example overlay. Note only one OperatorGroup per namespace is permitted by OpenShift.

```bash
kubectl apply -k overlays/grafana-uwm-user-app
```