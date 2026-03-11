# klgn-bioit-wiki

Helm chart for the KLGN Bio-IT Wiki application deployment to Azure AKS Kubernetes cluster.

## Structure

```
charts/
├── Chart.yaml           # Chart metadata
├── values.yaml          # Default configuration values
└── templates/
    ├── deployment.yaml  # Kubernetes Deployment template
    ├── service.yaml     # Kubernetes Service template
    └── _helpers.tpl     # Template helpers
```

## Usage

### Install the chart

```bash
helm install my-release ./charts
```

### Create a namespace and install

```bash
kubectl create namespace wiki
helm install wiki-release ./charts -n wiki
```

### Override values

```bash
helm install wiki-release ./charts \
  --set replicaCount=3 \
  --set image.tag=2.0
```

## Configuration

See `charts/values.yaml` for available configuration options.

## Branches

- **main**: Stable release branch
- **dev**: Development branch with latest changes
