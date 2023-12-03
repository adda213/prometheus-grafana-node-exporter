# prometheus-grafana-node-exporter

kubectl apply -f namespace.yml or kubectl create namespace monitoring

kubectl apply -f .

helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
helm install grafana grafana/grafana -n monitoring -f values.yml
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install [RELEASE_NAME] prometheus-community/prometheus-node-exporter
