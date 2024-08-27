# Grafana lab

In this example Grafana is deployed as `StatefulSet` with single pod.
The custom resource definition `OIDCClient` is used to automagically register
Grafana as OIDC client within
[Passmower](https://github.com/passmower/passmower)
IDP which is already deployed in the cluster.

Exercises:

* Replace `lauri` with your username
* Add `prometheus.yaml` in `grafana-datasources` ConfigMap to
  [declaratively configure data sources](https://grafana.com/docs/grafana/latest/administration/provisioning/) for Grafana
* Add CloudNativePG cluster into your sandbox or use existing one
* Reconfigure Grafana to use Postgres as backing store for Grafana,
  convert `StatefulSet` to `Deployment`
