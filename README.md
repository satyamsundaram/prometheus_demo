### Steps
1. start a k8s cluster in GKE
2. setup gcloud and kubectl locally to interact with the cluster
3. create namespace 'monitoring' in k8s for our current setup
4. deploy node-exporter in k8s cluster as a daemonset
5. create service account for kube-state-metrics as a deployment to collect cluster-level metrics
6. deploy prometheus and grafana locally using docker-compose
7. add node-exporter and kube-state-metrics as targets in prometheus using their external IPs
8. add prometheus as a datasource in grafana
9. import necessary dashboards in grafana
10. create an alert in prometheus for a cronjob not scheduling within a minute