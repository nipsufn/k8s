# hydra-maester

![Version: 0.57.1](https://img.shields.io/badge/Version-0.57.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.0.38](https://img.shields.io/badge/AppVersion-v0.0.38-informational?style=flat-square)

A Helm chart for Kubernetes

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| adminService.endpoint | string | `"/admin/clients"` | Set the clients endpoint, should be `/clients` for Hydra 1.x and `/admin/clients` for Hydra 2.x |
| adminService.insecureSkipVerify | bool | `false` | Skip http client insecure verification |
| adminService.name | string | `nil` | Service name |
| adminService.port | int | `4445` | Service port |
| adminService.scheme | string | `"http"` | Scheme used by Hydra client endpoint. May be "http" or "https" |
| adminService.tlsTrustStorePath | string | `""` | TLS ca-cert path for hydra client |
| affinity | object | `{}` | Configure node affinity |
| deployment.args | object | `{"syncPeriod":""}` | Arguments to be passed to the program |
| deployment.args.syncPeriod | string | `""` | The minimum frequency at which watched resources are reconciled |
| deployment.automountServiceAccountToken | bool | `true` | This applications connects to the k8s API and requires the permissions |
| deployment.dnsConfig | object | `{}` | Configure pod dnsConfig. |
| deployment.extraAnnotations | object | `{}` | Deployment level extra annotations |
| deployment.extraEnv | list | `[]` | To set extra env vars for the container. |
| deployment.extraLabels | object | `{}` | Deployment level extra labels |
| deployment.extraVolumeMounts | list | `[]` |  |
| deployment.extraVolumes | list | `[]` | If you want to mount external volume |
| deployment.nodeSelector | object | `{}` | Node labels for pod assignment. |
| deployment.podMetadata | object | `{"annotations":{},"labels":{}}` | Specify pod metadata, this metadata is added directly to the pod, and not higher objects |
| deployment.podMetadata.annotations | object | `{}` | Extra pod level annotations |
| deployment.podMetadata.labels | object | `{}` | Extra pod level labels |
| deployment.podSecurityContext.fsGroup | int | `65534` |  |
| deployment.podSecurityContext.fsGroupChangePolicy | string | `"OnRootMismatch"` |  |
| deployment.podSecurityContext.runAsGroup | int | `65534` |  |
| deployment.podSecurityContext.runAsNonRoot | bool | `true` |  |
| deployment.podSecurityContext.runAsUser | int | `65534` |  |
| deployment.podSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| deployment.resources | object | `{}` |  |
| deployment.securityContext.allowPrivilegeEscalation | bool | `false` |  |
| deployment.securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| deployment.securityContext.privileged | bool | `false` |  |
| deployment.securityContext.readOnlyRootFilesystem | bool | `true` |  |
| deployment.securityContext.runAsGroup | int | `65534` |  |
| deployment.securityContext.runAsNonRoot | bool | `true` |  |
| deployment.securityContext.runAsUser | int | `65534` |  |
| deployment.securityContext.seLinuxOptions.level | string | `"s0:c123,c456"` |  |
| deployment.securityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| deployment.serviceAccount | object | `{"annotations":{}}` | Configure service account |
| deployment.serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| deployment.terminationGracePeriodSeconds | int | `60` |  |
| deployment.tolerations | list | `[]` | Configure node tolerations. |
| deployment.topologySpreadConstraints | list | `[]` | Configure pod topologySpreadConstraints. |
| enabledNamespaces | list | `[]` | The Controller have CREATE and READ access to all Secrets in the namespaces listed below. |
| forwardedProto | string | `nil` |  |
| image.pullPolicy | string | `"IfNotPresent"` | Image pull policy |
| image.repository | string | `"oryd/hydra-maester"` | Ory Hydra-maester image |
| image.tag | string | `"v0.0.38"` | Ory Hydra-maester version |
| imagePullSecrets | list | `[]` | Image pull secrets |
| pdb.enabled | bool | `false` |  |
| pdb.spec.maxUnavailable | string | `""` |  |
| pdb.spec.minAvailable | string | `""` |  |
| priorityClassName | string | `""` | Pod priority # https://kubernetes.io/docs/concepts/configuration/pod-priority-preemption/ |
| replicaCount | int | `1` | Number of replicas in deployment |
| revisionHistoryLimit | int | `5` | Number of revisions kept in history |
| service.metrics.annotations | object | `{}` |  |
| service.metrics.enabled | bool | `false` |  |
| service.metrics.loadBalancerIP | string | `""` |  |
| service.metrics.name | string | `"http-metrics"` |  |
| service.metrics.port | int | `8080` |  |
| service.metrics.type | string | `"ClusterIP"` |  |
| serviceMonitor.labels | object | `{}` | Provide additional labels to the ServiceMonitor resource metadata |
| serviceMonitor.scheme | string | `"http"` | HTTP scheme to use for scraping. |
| serviceMonitor.scrapeInterval | string | `"60s"` | Interval at which metrics should be scraped |
| serviceMonitor.scrapeTimeout | string | `"30s"` | Timeout after which the scrape is ended |
| serviceMonitor.tlsConfig | object | `{}` | TLS configuration to use when scraping the endpoint |
| singleNamespaceMode | bool | `false` | Single namespace mode. If enabled the controller will watch for resources only from namespace it is deployed in, ignoring others |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
