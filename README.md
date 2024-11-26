# Federated Prometheus

The config will deploy a standalone prometheus and alertmanager.
It will scrape the /federated enpoint associated with prometheus-k8s-0 & prometheus-k8s-1 in openshift-monitoring. It's using the `kubernetes_sd_configs` for service discovery via the known name `prometheus-k8s.openshift-monitoring.svc.cluster.local`.

Sample alerts have been added via the configMap `configmap.general-rules.yaml` 


## TODO
The configfile alertmanger.yaml has not been defined as yet. 

Need to add an oauth config to both pods. Required for alertmanager as it's Read Write UI. Prometheus is not 100% required as it's a Read Only UI.
