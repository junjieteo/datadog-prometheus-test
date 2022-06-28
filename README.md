# Run the prometheus deployment locally
kubectl create -f prometheus.yaml

# Install the datadog agent
helm install datadog -f datadog-values.yaml --set datadog.site='datadoghq.com' --set datadog.apiKey='<api-key>' datadog/datadog