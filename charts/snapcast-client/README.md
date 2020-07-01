# snapcast-client

![Version: 0.1.5](https://img.shields.io/badge/Version-0.1.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.20.1](https://img.shields.io/badge/AppVersion-0.20.1-informational?style=flat-square)

A Helm chart for Kubernetes

**Homepage:** <https://github.com/grewhit25/my-helm-charts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| grewhit25 | grewhit25@gmail.com |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| extraVars.TZ | string | `"Europe/London"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.repository | string | `"docker.io/grewhit25/debian-snapclient"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| pulseaudio.enabled | bool | `false` |  |
| pulseaudio.mounts[0].hostpath | string | `"/var/run/pulse"` |  |
| pulseaudio.mounts[0].mountpath | string | `"/var/run/pulse"` |  |
| pulseaudio.mounts[0].name | string | `"var-run-pulse"` |  |
| pulseaudio.name | string | `"PULSE_SOCKET"` |  |
| pulseaudio.pulse_socket | string | `"unix:/var/run/pulse"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| tolerations | list | `[]` |  |
