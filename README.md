# GitOps Workflow with Kubernetes (Manifest Repository)
This is a separate repo for DevOps Assignment #5's Kubernetes manifests for use with ArgoCD as a GitOps operator.

- The Python Flask quiz application "Langy" is used in this assignment within the K8s deployments. ArgoCD  is watching the `k8s/overlays` directory ("app of apps" style) for changes to the dev and prod overlays.

- The overlays use base manifests then customize them using patch YAML files with Kustomize (replicas and resources differ between prod and dev).

- An encrypted secret is used with sealed-secrets.

- A CI workflow builds the final manifests and lints them before allowing merges from PRs.

- Self-healig and rollback are successfully implemented.

All screenshots can be found the in original assignment's repository [here](https://github.com/campus-wien-devops/assignment-5-jessicadraper/tree/main/screenshots).