# kratos-selfservice-ui-node

![Version: 0.57.1](https://img.shields.io/badge/Version-0.57.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.13.0-4](https://img.shields.io/badge/AppVersion-v0.13.0--4-informational?style=flat-square)

A Helm chart for ORY Kratos's example ui for Kubernetes

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| basePath | string | `""` | The basePath |
| config.csrfCookieName | string | `""` |  |
| config.secrets | object | `{}` |  |
| deployment.annotations | object | `{}` |  |
| deployment.automountServiceAccountToken | bool | `false` |  |
| deployment.dnsConfig | object | `{}` | Configure pod dnsConfig. |
| deployment.extraEnv | list | `[]` | Array of extra envs to be passed to the deployment. Kubernetes format is expected - name: FOO   value: BAR |
| deployment.extraVolumeMounts | list | `[]` |  |
| deployment.extraVolumes | list | `[]` | If you want to mount external volume For example, mount a secret containing Certificate root CA to verify database TLS connection. |
| deployment.labels | object | `{}` |  |
| deployment.nodeSelector | object | `{}` | Node labels for pod assignment. |
| deployment.resources | object | `{}` |  |
| deployment.terminationGracePeriodSeconds | int | `60` |  |
| deployment.tolerations | list | `[]` | Configure node tolerations. |
| deployment.topologySpreadConstraints | list | `[]` | Configure pod topologySpreadConstraints. |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"oryd/kratos-selfservice-ui-node"` |  |
| image.tag | string | `"v1.3.1"` | ORY KRATOS VERSION |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| jwksUrl | string | `"http://oathkeeper-api"` | The jwksUrl |
| kratosAdminUrl | string | `"http://kratos-admin"` | Set this to ORY Kratos's Admin URL |
| kratosBrowserUrl | string | `"http://kratos-browserui"` | Set this to ORY Kratos's public URL accessible from the outside world. |
| kratosPublicUrl | string | `"http://kratos-public"` | Set this to ORY Kratos's public URL |
| nameOverride | string | `""` |  |
| podSecurityContext.fsGroup | int | `10000` |  |
| podSecurityContext.fsGroupChangePolicy | string | `"OnRootMismatch"` |  |
| podSecurityContext.runAsGroup | int | `10000` |  |
| podSecurityContext.runAsNonRoot | bool | `true` |  |
| podSecurityContext.runAsUser | int | `10000` |  |
| podSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| projectName | string | `"SecureApp"` |  |
| replicaCount | int | `1` | Number of replicas in deployment |
| revisionHistoryLimit | int | `5` | Number of revisions kept in history |
| secret.enableDefaultAnnotations | bool | `true` | enableDefaultAnnotations set to `true` will add default annotations to the secret. As such the Secret will be managed by helm hooks. |
| secret.enabled | bool | `true` | switch to false to prevent creating the secret |
| secret.extraAnnotations | object | `{}` | extraAnnotations to be added to secret. |
| secret.hashSumEnabled | bool | `true` | switch to false to prevent checksum annotations being maintained and propogated to the pods |
| secret.nameOverride | string | `""` | Provide custom name of existing secret, or custom name of secret to be created |
| secret.secretAnnotations | object | `{"helm.sh/hook":"pre-install, pre-upgrade","helm.sh/hook-delete-policy":"before-hook-creation","helm.sh/hook-weight":"0","helm.sh/resource-policy":"keep"}` | Annotations to be added to secret. Annotations are added only when secret is being created. Existing secret will not be modified. |
| securityContext.allowPrivilegeEscalation | bool | `false` |  |
| securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| securityContext.privileged | bool | `false` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| securityContext.runAsGroup | int | `10000` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `10000` |  |
| securityContext.seLinuxOptions.level | string | `"s0:c123,c456"` |  |
| securityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| service.annotations | object | `{}` | If you do want to specify annotations, uncomment the following lines, adjust them as necessary, and remove the curly braces after 'annotations:'. |
| service.enabled | bool | `true` |  |
| service.labels | object | `{}` | Provide custom labels. Use the same syntax as for annotations. |
| service.loadBalancerIP | string | `""` | The load balancer IP |
| service.name | string | `"http"` | The service port name. Useful to set a custom service port name if it must follow a scheme (e.g. Istio) |
| service.nodePort | string | `""` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| test.busybox | object | `{"repository":"busybox","tag":1}` | use a busybox image from another repository |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
