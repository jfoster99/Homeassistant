# Home Assistant GitOps Deployment

This repository manages the deployment of Home Assistant using Helm and ArgoCD, following GitOps best practices.

## Structure

- `apps/homeassistant/base/`: Base Kustomize and ArgoCD Application manifest for Home Assistant.
- `apps/homeassistant/overlays/prod/`: Production-specific overrides and values.
- `charts/`: (Optional) Place for custom or local Helm charts.

## Usage

1. **Register the Application with ArgoCD:**
   - Point ArgoCD to the `apps/homeassistant/base` or an overlay (e.g., `overlays/prod`) as the application path.
2. **Sync the Application:**
   - ArgoCD will deploy Home Assistant using the specified Helm chart and values.
3. **Customize:**
   - Edit the `values-prod.yaml` or add new overlays for other environments.

## Requirements
- ArgoCD instance
- Kubernetes cluster
- (Optional) Custom domain and TLS for production

---

For more details, see the manifests in `apps/homeassistant/`.
