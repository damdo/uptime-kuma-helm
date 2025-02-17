# uptime-kuma

![Version: 2.9.3](https://img.shields.io/badge/Version-2.9.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.21.3](https://img.shields.io/badge/AppVersion-1.21.3-informational?style=flat-square)

A self-hosted Monitoring tool like "Uptime-Robot".

**Homepage:** <https://github.com/dirsigler/uptime-kuma-helm>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| dirsigler | <dennis@irsigler.dev> |  |

## Source Code

* <https://github.com/louislam/uptime-kuma>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"louislam/uptime-kuma"` |  |
| image.tag | string | `"1.21.3-debian"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/proxy-read-timeout" | string | `"3600"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/proxy-send-timeout" | string | `"3600"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/server-snippets" | string | `"location / {\n  proxy_set_header Upgrade $http_upgrade;\n  proxy_http_version 1.1;\n  proxy_set_header X-Forwarded-Host $http_host;\n  proxy_set_header X-Forwarded-Proto $scheme;\n  proxy_set_header X-Forwarded-For $remote_addr;\n  proxy_set_header Host $host;\n  proxy_set_header Connection \"upgrade\";\n  proxy_set_header X-Real-IP $remote_addr;\n  proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;\n  proxy_set_header   Upgrade $http_upgrade;\n  proxy_cache_bypass $http_upgrade;\n}\n"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.extraLabels | object | `{}` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.initialDelaySeconds | int | `15` |  |
| livenessProbe.timeoutSeconds | int | `2` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podEnv[0].name | string | `"UPTIME_KUMA_PORT"` |  |
| podEnv[0].value | string | `"3001"` |  |
| podLabels | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.initialDelaySeconds | int | `5` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.annotations | object | `{}` |  |
| service.nodePort | string | `nil` |  |
| service.port | int | `3001` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| strategy.type | string | `"Recreate"` |  |
| tolerations | list | `[]` |  |
| useDeploy | bool | `true` |  |
| volume.accessMode | string | `"ReadWriteOnce"` |  |
| volume.enabled | bool | `true` |  |
| volume.existingClaim | string | `""` |  |
| volume.size | string | `"4Gi"` |  |

