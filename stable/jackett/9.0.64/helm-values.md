# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | `{}` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/jackett"` |  |
| image.tag | string | `"v0.20.280@sha256:12ba13c2b70fdbd1270eda69a60e919b4bc6400d2df338635667d2111b70d619"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/config"` |  |
| probes.liveness.path | string | `"/UI/Login"` |  |
| probes.readiness.path | string | `"/UI/Login"` |  |
| probes.startup.path | string | `"/UI/Login"` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| service.main.ports.main.port | int | `9117` |  |
| service.main.ports.main.targetPort | int | `9117` |  |
| service.main.protocol | string | `"HTTP"` |  |

All Rights Reserved - The TrueCharts Project
