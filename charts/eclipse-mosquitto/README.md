# eclipse-mosquitto

![Version: 1.0.2](https://img.shields.io/badge/Version-1.0.2-informational?style=flat-square) ![AppVersion: 1.6.10](https://img.shields.io/badge/AppVersion-1.6.10-informational?style=flat-square)

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
| certs.ca.crt | string | `"-----BEGIN CERTIFICATE-----\nCA_CERT\n-----END CERTIFICATE-----"` |  |
| certs.server.crt | string | `"-----BEGIN CERTIFICATE-----\nSERVER_CERT\n-----END CERTIFICATE-----"` |  |
| certs.server.key | string | `"-----BEGIN PRIVATE KEY-----\nSERVER_KEY\n-----END PRIVATE KEY-----"` |  |
| config | string | `"persistence true\npersistence_location /mosquitto/data/\nlog_dest stdout\nlog_type error\nlog_type warning\nlog_type information\nlistener 1883\nlistener 9001\nprotocol websockets\ncafile /mosquitto/config/certs/ca.crt\ncertfile /mosquitto/config/certs/server.crt\nkeyfile /mosquitto/config/certs/server.key\nrequire_certificate true\nuse_subject_as_username true\nhttp_dir /health"` |  |
| extraVars.http_dir | string | `"/health"` |  |
| fullnameOverride | string | `""` |  |
| healthz | string | `"\"Hello World!\""` |  |
| healthzscript | string | `"#!/bin/sh\nmosquitto_sub -i \"ReadyLivenessProbe\" -t '$SYS/#' -C 1 \\\n| grep -q -e \"mosquitto version\" \\\n> /dev/null 2>&1 || exit 1"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"eclipse-mosquitto"` |  |
| image.tag | string | `"1.6.10"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."cert-manager.io/issuer" | string | `"alpha-selfcert-ca-issuer"` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"mqtt.server.svc.alpha.local"` |  |
| ingress.hosts[0].paths[0] | string | `"/"` |  |
| ingress.tls[0].hosts[0] | string | `"mqtt.server.svc.alpha.local"` |  |
| ingress.tls[0].secretName | string | `"mqtt-server-ingress-tls"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| persistence.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.annotations | object | `{}` |  |
| persistence.enabled | bool | `false` |  |
| persistence.size | string | `"1Gi"` |  |
| persistence.storageClass | string | `"managed-nfs-storage"` |  |
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
