# metric-store-exporter-release

A boshrelease to deploy prometheus exporter to export metric from a [cloud foundry metric-store](https://github.com/cloudfoundry/metric-store-release).

# deploy

1. Add ops file [/manifests/operations/metric-store/metric-store.yml](/manifests/operations/metric-store/metric-store.yml) to where you deploy you metric store
2. bosh deploy
3. access to metric by accessing to `http://<vm-ip>:8086/metrics` and optionally filter by metric name with `http://<vm-ip>:8086/metrics?metric[]=metric_1&metric[]=metric_2&...`