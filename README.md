# CloudPhilos Helm Charts

Official Helm charts for CloudPhilos Outbound monitoring solutions.

## Usage

Add the CloudPhilos Helm repository:

```bash
helm repo add cloudphilos https://charts.cloudphilos.net
helm repo update
```

Search available charts:

```bash
helm search repo cloudphilos
```

## Available Charts

| Chart | Description | Documentation |
|-------|-------------|---------------|
| [outbound-k8s-sensor](./outbound-k8s-sensor) | Kubernetes pod monitoring sensor for CloudPhilos Outbound | [README](./outbound-k8s-sensor/README.md) |

## Configuration

Each chart includes a `values.yaml` file with default values. You can override these values during installation:

```bash
helm install my-release cloudphilos/chart-name \
  --set key1=value1 \
  --set key2=value2
```

Or use a custom values file:

```bash
helm install my-release cloudphilos/chart-name -f custom-values.yaml
```

## Support

- **Issues**: https://github.com/cloudphilos/outbound-charts/issues
