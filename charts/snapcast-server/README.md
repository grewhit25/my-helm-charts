# snapcast-server

![Version: 0.1.1](https://img.shields.io/badge/Version-0.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.20.1](https://img.shields.io/badge/AppVersion-0.20.1-informational?style=flat-square)

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
| avahiEnabled | string | `"true"` |  |
| extraVars.LIVENESS_CHECK | string | `"cat /health/healthz"` |  |
| extraVars.READINESS_CHECK | string | `"cat /health/healthz"` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.repository | string | `"docker.io/grewhit25/debian-snapserver"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| ports.server.port | int | `1705` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| service.annotations | object | `{}` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `nil` |  |
| snapcast_serverConfig | string | `"[stream]\nstream = \"pipe:///output/mpd_fifo?name=tts&sampleformat=44100:16:2&codec=flac\"\nstream = \"pipe:///output/mopidy_fifo?name=Mopidy&sampleformat=44100:16:2&codec=flac\"\nstream = \"spotify:///librespot?name=Spotify&verbose&cache=/tmp&device=Snapcast&bitrate=320&initial-volume=75&sampleformat=44100:16:2&codec=flac\""` |  |
| tolerations | list | `[]` |  |