# Awesome All In SKL

## Component description of DevOps style
- conf_nginx (config for nginx)
- helm-chart (templates for deploy via helm)
- jenkins-master (values for deploy jenkins)
- k8s (values for deploy app)
- pipeline (config for CI/CD step)
- Dockerfile (for build image of app)
- docker-compose (for full stack on container app)

## Docker Compose give to Developer everting จิงเกอเบล
```bash
# for Build
docker-compose build

# for start services
docker-compose up
```
#### Environment default
> in docker-compose.yaml \
you can edit ENV, all right

---

## Era of the HELMMMM !!!
WE ARE REQUIRED HELM VERISON >= 3.0.0 \
FOR MANUAL DEPLOY VIA HELM
```bash
## Install new RELEASE to Cluster
helm install -f {VALUE_FILE}.yaml {RELEASE_NAME} {HELM_CHART}

## Upgrade new version to Cluster
# You can specific value file for overwrite stage.
helm upgrade -f {VALUE_FILE}.yaml {RELEASE_NAME} {HELM_CHART}

# Uninstall RELEASE
helm uninstall {RELEASE_NAME}
```
#### Environment default
> in k8s >> helm >> values-{stage}.yaml \
you can edit ENV, all right