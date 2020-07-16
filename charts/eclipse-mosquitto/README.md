# eclipse-mosquitto

![Version: 2.0.0](https://img.shields.io/badge/Version-2.0.0-informational?style=flat-square) ![AppVersion: 1.6.10](https://img.shields.io/badge/AppVersion-1.6.10-informational?style=flat-square)

A Helm chart for Eclipse Mosquitto

**Homepage:** <https://github.com/grewhit25/my-helm-charts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| grewhit25 | grewhit25@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| config | string | `"persistence true\npersistence_location /mosquitto/data/\nlog_dest stdout\nlistener 1883\nlistener 9001\nprotocol mqtt"` |  |
| extraVars | object | `{}` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"eclipse-mosquitto"` |  |
| image.tag | string | `"1.6.10"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"mqtt.server.local"` |  |
| ingress.hosts[0].paths[0] | string | `"/"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.enabled | bool | `false` |  |
| persistence.size | string | `"1Gi"` |  |
| ports.mqtt.name | string | `"mqtt"` |  |
| ports.mqtt.port | int | `1883` |  |
| ports.mqtt.protocol | string | `"TCP"` |  |
| ports.websocket.name | string | `"websocket"` |  |
| ports.websocket.port | int | `9001` |  |
| ports.websocket.protocol | string | `"TCP"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext.enabled | bool | `false` |  |
| securityContext.fsGroup | int | `999` |  |
| securityContext.runAsUser | int | `999` |  |
| service.annotations | object | `{}` |  |
| service.type | string | `"ClusterIP"` |  |
| tolerations | list | `[]` |  |
