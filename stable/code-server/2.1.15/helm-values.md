# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| args[0] | string | `"--user-data-dir"` |  |
| args[1] | string | `"/config/.vscode"` |  |
| args[2] | string | `"--auth"` |  |
| args[3] | string | `"none"` |  |
| env | object | `{}` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/code-server"` |  |
| image.tag | string | `"v4.0.1@sha256:d9a55822e344aaacfca5151fa2b7e7bb79dd1170bb348ae34c6e74954cc9a85d"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/config"` |  |
| securityContext.allowPrivilegeEscalation | bool | `true` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| service.main.ports.main.port | int | `10063` |  |
| service.main.ports.main.targetPort | int | `8080` |  |

All Rights Reserved - The TrueCharts Project
