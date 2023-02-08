# hive-metastore

![Version: 0.0.1](https://img.shields.io/badge/Version-0.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 3.0.0](https://img.shields.io/badge/AppVersion-3.0.0-informational?style=flat-square)

Helm chart to deploy [hive-metastore](https://hive.apache.org/).

**Homepage:** <https://github.com/bitsondatadev/hive-metastore/chart>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| bitsondatadev | brianolsen87@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | affinity for scheduler pod assignment |
| env | list | `[]` | additional environment variables for the deployment |
| fullnameOverride | string | `""` | full name of the chart. |
| hiveSiteXml | string | `"<configuration>\n\n</configuration>\n"` |  |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"slamdev/apache-hive"` | image repository |
| image.tag | string | `""` | image tag (chart's appVersion value will be used if not set) |
| imagePullSecrets | list | `[]` | image pull secret for private images |
| importJars.coords | list | `[]` | maven coords |
| importJars.enabled | bool | `false` | import jars as init container |
| ingress.annotations | object | `{}` | ingress annotations |
| ingress.enabled | bool | `false` | enables Ingress for hive-metastore |
| ingress.hosts | list | `[]` | ingress accepted hostnames |
| ingress.tls | list | `[]` | ingress TLS configuration |
| initContainers | list | `[]` | additional init containers; env vars and volume mounts are the same as for the main container |
| nameOverride | string | `""` | override name of the chart |
| nodeSelector | object | `{}` | node for scheduler pod assignment |
| podSecurityContext | object | `{}` | specifies security settings for a pod |
| replicaCount | int | `1` | number of replicas for flux-notifier deployment. |
| resources | object | `{}` | custom resource configuration |
| schematool.dbType | string | `"postgres"` | schematool database type |
| schematool.enabled | bool | `false` | run schematool as init container |
| securityContext | object | `{}` | specifies security settings for a container |
| service.port | int | `9083` | service port |
| service.type | string | `"ClusterIP"` | service type |
| serviceAccount.annotations | object | `{}` | annotations to add to the service account |
| serviceAccount.create | bool | `false` | specifies whether a service account should be created |
| serviceAccount.name | string | `nil` | the name of the service account to use; if not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` | tolerations for scheduler pod assignment |
| volumeMounts | list | `[]` | additional volume mounts |
| volumes | list | `[]` | additional volumes |
