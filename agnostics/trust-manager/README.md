# Trust-Manager for K8TRE

Trust-manager creates a shared certificate authority (CA) bundle that can optionally be mounted into pods.
This includes a standard CA bundle, with the addition of an internal private CA.

Learn more at [https://cert-manager.io/docs/trust/trust-manager/](https://cert-manager.io/docs/trust/trust-manager/)

## Structure

- `base/` - Contains the base Kubernetes manifests including ClusterIssuer configurations
- `azure/` - Azure-specific configurations
- `k3s/` - K3S-specific configurations
- `envs/` - Environment-specific configurations (dev/stg/prd)

## Vendor Differences

The implementation differs between Azure and K3S deployments. K3S deployments include self-signed certificate issuers for development environments, while Azure deployments may integrate with Azure-native certificate services.
