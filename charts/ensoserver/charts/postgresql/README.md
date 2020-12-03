postgresql
==========
Chart for PostgreSQL, an object-relational database management system (ORDBMS) with an emphasis on extensibility and on standards-compliance.

Current chart version is `10.1.1`

Source code can be found [here](https://github.com/bitnami/charts/tree/master/bitnami/postgresql)

## Chart Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 1.x.x |

## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| audit.clientMinMessages | string | `"error"` |  |
| audit.logConnections | bool | `false` |  |
| audit.logDisconnections | bool | `false` |  |
| audit.logHostname | bool | `false` |  |
| audit.logLinePrefix | string | `""` |  |
| audit.logTimezone | string | `""` |  |
| audit.pgAuditLog | string | `""` |  |
| audit.pgAuditLogCatalog | string | `"off"` |  |
| commonAnnotations | object | `{}` |  |
| containerSecurityContext.enabled | bool | `true` |  |
| containerSecurityContext.runAsUser | int | `1001` |  |
| customLivenessProbe | object | `{}` |  |
| customReadinessProbe | object | `{}` |  |
| extraDeploy | list | `[]` |  |
| extraEnv | list | `[]` |  |
| global.postgresql | object | `{}` |  |
| image.debug | bool | `false` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"bitnami/postgresql"` |  |
| image.tag | string | `"11.10.0-debian-10-r9"` |  |
| ldap.baseDN | string | `""` |  |
| ldap.bindDN | string | `""` |  |
| ldap.bind_password | string | `nil` |  |
| ldap.enabled | bool | `false` |  |
| ldap.port | string | `""` |  |
| ldap.prefix | string | `""` |  |
| ldap.scheme | string | `""` |  |
| ldap.search_attr | string | `""` |  |
| ldap.search_filter | string | `""` |  |
| ldap.server | string | `""` |  |
| ldap.suffix | string | `""` |  |
| ldap.tls | object | `{}` |  |
| ldap.url | string | `""` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `6` |  |
| livenessProbe.initialDelaySeconds | int | `30` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| metrics.enabled | bool | `false` |  |
| metrics.extraEnvVars | object | `{}` |  |
| metrics.image.pullPolicy | string | `"IfNotPresent"` |  |
| metrics.image.registry | string | `"docker.io"` |  |
| metrics.image.repository | string | `"bitnami/postgres-exporter"` |  |
| metrics.image.tag | string | `"0.8.0-debian-10-r278"` |  |
| metrics.livenessProbe.enabled | bool | `true` |  |
| metrics.livenessProbe.failureThreshold | int | `6` |  |
| metrics.livenessProbe.initialDelaySeconds | int | `5` |  |
| metrics.livenessProbe.periodSeconds | int | `10` |  |
| metrics.livenessProbe.successThreshold | int | `1` |  |
| metrics.livenessProbe.timeoutSeconds | int | `5` |  |
| metrics.prometheusRule.additionalLabels | object | `{}` |  |
| metrics.prometheusRule.enabled | bool | `false` |  |
| metrics.prometheusRule.namespace | string | `""` |  |
| metrics.prometheusRule.rules | list | `[]` |  |
| metrics.readinessProbe.enabled | bool | `true` |  |
| metrics.readinessProbe.failureThreshold | int | `6` |  |
| metrics.readinessProbe.initialDelaySeconds | int | `5` |  |
| metrics.readinessProbe.periodSeconds | int | `10` |  |
| metrics.readinessProbe.successThreshold | int | `1` |  |
| metrics.readinessProbe.timeoutSeconds | int | `5` |  |
| metrics.securityContext.enabled | bool | `false` |  |
| metrics.securityContext.runAsUser | int | `1001` |  |
| metrics.service.annotations."prometheus.io/port" | string | `"9187"` |  |
| metrics.service.annotations."prometheus.io/scrape" | string | `"true"` |  |
| metrics.service.loadBalancerIP | string | `nil` |  |
| metrics.service.type | string | `"ClusterIP"` |  |
| metrics.serviceMonitor.additionalLabels | object | `{}` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| networkPolicy.allowExternal | bool | `true` |  |
| networkPolicy.enabled | bool | `false` |  |
| networkPolicy.explicitNamespacesSelector | object | `{}` |  |
| persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.enabled | bool | `true` |  |
| persistence.mountPath | string | `"/bitnami/postgresql"` |  |
| persistence.selector | object | `{}` |  |
| persistence.size | string | `"8Gi"` |  |
| persistence.subPath | string | `""` |  |
| postgresqlDataDir | string | `"/bitnami/postgresql/data"` |  |
| postgresqlDbUserConnectionLimit | string | `nil` |  |
| postgresqlMaxConnections | string | `nil` |  |
| postgresqlPghbaRemoveFilters | string | `nil` |  |
| postgresqlPostgresConnectionLimit | string | `nil` |  |
| postgresqlSharedPreloadLibraries | string | `"pgaudit"` |  |
| postgresqlStatementTimeout | string | `nil` |  |
| postgresqlTcpKeepalivesCount | string | `nil` |  |
| postgresqlTcpKeepalivesIdle | string | `nil` |  |
| postgresqlTcpKeepalivesInterval | string | `nil` |  |
| postgresqlUsername | string | `"postgres"` |  |
| primary.affinity | object | `{}` |  |
| primary.annotations | object | `{}` |  |
| primary.extraInitContainers | list | `[]` |  |
| primary.extraVolumeMounts | list | `[]` |  |
| primary.extraVolumes | list | `[]` |  |
| primary.labels | object | `{}` |  |
| primary.nodeSelector | object | `{}` |  |
| primary.podAnnotations | object | `{}` |  |
| primary.podLabels | object | `{}` |  |
| primary.priorityClassName | string | `""` |  |
| primary.service | object | `{}` |  |
| primary.sidecars | list | `[]` |  |
| primary.tolerations | list | `[]` |  |
| primaryAsStandBy.enabled | bool | `false` |  |
| psp.create | bool | `false` |  |
| rbac.create | bool | `false` |  |
| readReplicas.affinity | object | `{}` |  |
| readReplicas.annotations | object | `{}` |  |
| readReplicas.extraInitContainers | list | `[]` |  |
| readReplicas.extraVolumeMounts | list | `[]` |  |
| readReplicas.extraVolumes | list | `[]` |  |
| readReplicas.labels | object | `{}` |  |
| readReplicas.nodeSelector | object | `{}` |  |
| readReplicas.persistence.enabled | bool | `true` |  |
| readReplicas.podAnnotations | object | `{}` |  |
| readReplicas.podLabels | object | `{}` |  |
| readReplicas.priorityClassName | string | `""` |  |
| readReplicas.resources | object | `{}` |  |
| readReplicas.service | object | `{}` |  |
| readReplicas.sidecars | list | `[]` |  |
| readReplicas.tolerations | list | `[]` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `6` |  |
| readinessProbe.initialDelaySeconds | int | `5` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `5` |  |
| replication.applicationName | string | `"my_application"` |  |
| replication.enabled | bool | `false` |  |
| replication.numSynchronousReplicas | int | `0` |  |
| replication.password | string | `"repl_password"` |  |
| replication.readReplicas | int | `1` |  |
| replication.synchronousCommit | string | `"off"` |  |
| replication.user | string | `"repl_user"` |  |
| resources.requests.cpu | string | `"250m"` |  |
| resources.requests.memory | string | `"256Mi"` |  |
| securityContext.enabled | bool | `true` |  |
| securityContext.fsGroup | int | `1001` |  |
| service.annotations | object | `{}` |  |
| service.port | int | `5432` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.enabled | bool | `false` |  |
| shmVolume.chmod.enabled | bool | `true` |  |
| shmVolume.enabled | bool | `true` |  |
| tls.certCAFilename | string | `nil` |  |
| tls.certFilename | string | `""` |  |
| tls.certKeyFilename | string | `""` |  |
| tls.certificatesSecret | string | `""` |  |
| tls.crlFilename | string | `nil` |  |
| tls.enabled | bool | `false` |  |
| tls.preferServerCiphers | bool | `true` |  |
| updateStrategy.type | string | `"RollingUpdate"` |  |
| volumePermissions.enabled | bool | `false` |  |
| volumePermissions.image.pullPolicy | string | `"Always"` |  |
| volumePermissions.image.registry | string | `"docker.io"` |  |
| volumePermissions.image.repository | string | `"bitnami/minideb"` |  |
| volumePermissions.image.tag | string | `"buster"` |  |
| volumePermissions.securityContext.runAsUser | int | `0` |  |
