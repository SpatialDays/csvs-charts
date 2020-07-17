terria
======
A Helm chart for terria map

Current chart version is `0.14.1`

Source code can be found [here](https://terria.io/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| authentication.enabled | bool | `false` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| clientConfig.initializationUrls[0] | string | `"terria"` |  |
| clientConfig.parameters.appName | string | `"Terria Map"` |  |
| clientConfig.parameters.brandBarElements[0] | string | `""` |  |
| clientConfig.parameters.brandBarElements[1] | string | `"<a target=\"_blank\" href=\"http://terria.io\"><img src=\"images/terria_logo.png\" height=\"52\" title=\"Version: {{version}}\" /></a>"` |  |
| clientConfig.parameters.brandBarElements[2] | string | `""` |  |
| clientConfig.parameters.disclaimer.text | string | `"Disclaimer: This map must not be used for navigation or precise spatial analysis"` |  |
| clientConfig.parameters.disclaimer.url | string | `""` |  |
| clientConfig.parameters.experimentalFeatures | bool | `true` |  |
| clientConfig.parameters.feedbackUrl | string | `"feedback"` |  |
| clientConfig.parameters.googleAnalyticsKey | string | `nil` |  |
| clientConfig.parameters.googleAnalyticsOptions | string | `nil` |  |
| clientConfig.parameters.googleUrlShortenerKey | string | `nil` |  |
| clientConfig.parameters.mobileDefaultViewerMode | string | `"2d"` |  |
| clientConfig.parameters.proj4ServiceBaseUrl | string | `"proj4def/"` |  |
| clientConfig.parameters.supportEmail | string | `"help@example.com"` |  |
| clientConfig.parameters.useCesiumIonBingImagery | bool | `false` |  |
| clientConfig.parameters.useCesiumIonTerrain | bool | `false` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"satapps/terriamap"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/rewrite-target" | string | `"/$1"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0].host | string | `"dev-csvs.sa-catapult.co.uk"` |  |
| ingress.hosts[0].paths[0].path | string | `"/terria-solomon/(.*)"` |  |
| ingress.tls | list | `[]` |  |
| initConfig.baseMapName | string | `"Positron (Light)"` |  |
| initConfig.catalog[0].geoserverWorkspace | string | `"solomon"` |  |
| initConfig.catalog[0].groupDescription | string | `"This group contains DRR vector data for Solomon Island"` |  |
| initConfig.catalog[0].groupName | string | `"DRR"` |  |
| initConfig.catalog[0].groupType | string | `"wfs-getCapabilities"` |  |
| initConfig.catalog[1].geoserverWorkspace | string | `"solomon_rasters"` |  |
| initConfig.catalog[1].groupDescription | string | `"This group contains maps of Hazard for Solomon Island"` |  |
| initConfig.catalog[1].groupName | string | `"Hazard data"` |  |
| initConfig.catalog[1].groupType | string | `"wms-getCapabilities"` |  |
| initConfig.homeCamera.east | int | `177` |  |
| initConfig.homeCamera.north | int | `-5` |  |
| initConfig.homeCamera.south | int | `-24` |  |
| initConfig.homeCamera.west | int | `152` |  |
| initConfig.viewMode | string | `"2d"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| serverConfig.geoserverBaseUrl | string | `"geoserver:8080"` |  |
| serverConfig.geoserverCredentials | string | `"test_user:test_password"` |  |
| service.port | int | `3001` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
