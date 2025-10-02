# CloudPhilos Outbound Kubernetes Sensor

The CloudPhilos Outbound Kubernetes Sensor monitors pod lifecycle events in your Kubernetes cluster and reports egress IP information to the CloudPhilos platform.

## Installation

```bash
# Add the CloudPhilos Helm repository
helm repo add cloudphilos https://charts.cloudphilos.net
helm repo update

# Create namespace
kubectl create namespace outbound-system

# Install the chart
helm install outbound-k8s-sensor cloudphilos/outbound-k8s-sensor \
  --namespace outbound-system \
  --set env.tenantId=YOUR_TENANT_ID
```

## Configuration

All configuration is done through the `values.yaml` file. You can override values during installation:

```bash
helm install outbound-k8s-sensor cloudphilos/outbound-k8s-sensor \
  --namespace outbound-system \
  --set key1=value1 \
  --set key2=value2
```

Or use a custom values file:

```bash
helm install outbound-k8s-sensor cloudphilos/outbound-k8s-sensor \
  --namespace outbound-system \
  -f custom-values.yaml
```

## Documentation

- [Full Deployment Guide](https://docs.cloudphilos.net/outbound/kubernetes-sensor)
- [Source Code Repository](https://github.com/cloudphilos/outbound-k8s-sensor)

## Support

- **Documentation**: https://docs.cloudphilos.net
- **Support**: support@cloudphilos.net
- **Issues**: https://github.com/cloudphilos/outbound-charts/issues
