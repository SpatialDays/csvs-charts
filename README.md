helm-geoserver-postgres
=======================

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)
![](https://github.com/SatelliteApplicationsCatapult/helm-geoserver-postgres/workflows/release/badge.svg)
![Release](https://github.com/SatelliteApplicationsCatapult/helm-geoserver-postgres/workflows/Release/badge.svg)

A Helm chart for Kubernetes

## Usage

1. Install [Helm](https://helm.sh). For more information, see [Helm documentation](https://helm.sh/docs/).

2. Add the helm-geoserver-postgres Helm repository:

```console
$ helm repo add helm-geoserver-postgres https://SatelliteApplicationsCatapult.github.io/helm-geoserver-postgres
$ helm repo update
```

3. View helm-geoserver-postgres Helm charts:

 ```console
 $ helm search helm-geoserver-postgres
 ```



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"davidedelerma/geoserver"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"kubernetes.docker.internal"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `6` |  |
| livenessProbe.initialDelaySeconds | int | `60` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| pvc.remote.name | string | `"dev-geoserver-csvs"` |  |
| pvc.remote.namespace | string | `"dev-csvs"` |  |
| pvc.remote.storageClassName | string | `"fast"` |  |
| readinessProbe.enabled | bool | `true` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `8080` |  |
| service.type | string | `"LoadBalancer"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| tolerations | list | `[]` |  |