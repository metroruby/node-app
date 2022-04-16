# Helm-NodeJS

WE ARE REQUIRED HELM VERISON >= 3.0.0

## Install new RELEASE to Cluster

```bash
helm install {RELEASE_NAME} .
```
---
## Upgrade new version to Cluster

You can specific value file for overwrite stage.

```bash
helm upgrade {-f value-{stage}.yaml} {RELEASE_NAME} .
```
---
## Uninstall RELEASE
```bash
helm uninstall {RELEASE_NAME}
```
