# snapcast-client

![Version: 1.0.2](https://img.shields.io/badge/Version-1.0.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.20.0](https://img.shields.io/badge/AppVersion-0.20.0-informational?style=flat-square)

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
| avahiEnabled | bool | `true` |  |
| extraVars.LIVENESS_CHECK | string | `"cat /health/healthz"` |  |
| extraVars.READINESS_CHECK | string | `"cat /health/healthz"` |  |
| extraVars.TZ | string | `"Europe/London"` |  |
| fullnameOverride | string | `""` |  |
| hostNetwork | bool | `true` |  |
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
| probes.liveness.enabled | bool | `false` |  |
| probes.liveness.failureThreshold | int | `5` |  |
| probes.liveness.initialDelaySeconds | int | `15` |  |
| probes.liveness.scheme | string | `"HTTP"` |  |
| probes.liveness.timeoutSeconds | int | `10` |  |
| probes.readiness.enabled | bool | `false` |  |
| probes.readiness.failureThreshold | int | `5` |  |
| probes.readiness.initialDelaySeconds | int | `15` |  |
| probes.readiness.scheme | string | `"HTTP"` |  |
| probes.readiness.timeoutSeconds | int | `10` |  |
| probes.startup.enabled | bool | `false` |  |
| probes.startup.failureThreshold | int | `30` |  |
| probes.startup.periodSeconds | int | `10` |  |
| probes.startup.scheme | string | `"HTTP"` |  |
| pulseaudio.enabled | bool | `true` |  |
| pulseaudio.extraEnv | object | `{}` |  |
| pulseaudio.name | string | `"PULSE_SERVER"` |  |
| pulseaudio.server | string | `"tcp:10.0.1.1:4713"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.port | int | `4713` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| tolerations | list | `[]` |  |
