# Deploy WebApp Demo (CloudLabs)

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/cyberlab-cley-security/deploy-webapp-demo/Build%20%26%20Deploy?label=CI/CD&logo=github)  

This repository contains the Kubernetes manifests and Kustomize configuration for deploying a demo version of the **CloudLabs WebApp**. It’s tailored for GitOps workflows using **ArgoCD**, and supports dynamic Docker image tagging.

## 🚀 Features

- **Declarative Kubernetes resources**: Namespace, ConfigMap, Secret, Deployment, Service, ServiceAccount, RBAC.
- **Kustomize-based image versioning**: Easily override Docker image tags in `kustomization.yaml`.
- **GitOps ready**: Designed to be deployed by ArgoCD with automated sync.
- **CI/CD integration**: Can be used with GitHub Actions or any CI to build, tag, and deploy.

## 📁 Repository Structure

```bash
deploy-webapp-demo/
├── deployment.yaml # All Kubernetes manifests (Namespace, Deployment, etc.)
└── kustomization.yaml # Kustomize configuration to override image tag
```

## ⚙️ CI/CD Integration

Here is a sample workflow to:

* Build & push the Docker image
* Update `kustomization.yaml` with the new tag
* Commit & push the change
* Trigger an ArgoCD sync

---

## 📚 References

* [ArgoCD Kustomize docs](https://argo-cd.readthedocs.io/en/stable/user-guide/kustomize/)
* [ArgoCD Best Practices](https://argo-cd.readthedocs.io/en/stable/operator-manual/best_practices/)

---

## 📄 License

This project is licensed under the MIT License — see the `LICENSE` file for details.