# awx

![Version: 0.6.0](https://img.shields.io/badge/Version-0.6.0-informational?style=flat-square) ![AppVersion: 6.1.0](https://img.shields.io/badge/AppVersion-6.1.0-informational?style=flat-square)

Installs Ansible AWX (Ansible Web UI), with dependencies (rabbitmq, postgresql, memcahed)

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| kim0 | <email.ahmedkamal@googlemail.com> |  |

## Source Code

* <https://github.com/ansible/awx>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://kubernetes-charts.storage.googleapis.com/ | memcached | 2.9.0 |
| https://kubernetes-charts.storage.googleapis.com/ | postgresql | 6.2.0 |
| https://kubernetes-charts.storage.googleapis.com/ | rabbitmq | 6.2.6 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| awx_secret_key | string | `"awxsecret"` |  |
| awx_task.image.pullPolicy | string | `"IfNotPresent"` |  |
| awx_task.image.repository | string | `"ansible/awx_task"` |  |
| awx_task.image.tag | string | `"9.1.0"` |  |
| awx_url_base | string | `"https://towerhost"` |  |
| awx_web.image.pullPolicy | string | `"IfNotPresent"` |  |
| awx_web.image.repository | string | `"ansible/awx_web"` |  |
| awx_web.image.tag | string | `"9.1.0"` |  |
| default_admin_password | string | `"password"` |  |
| default_admin_user | string | `"admin"` |  |
| default_from_email | string | `"webmaster@localhost"` |  |
| deployment.annotations | object | `{}` |  |
| email_host | string | `"localhost"` |  |
| email_host_password | string | `""` |  |
| email_host_user | string | `""` |  |
| email_port | int | `25` |  |
| email_subject_prefix | string | `"[AWX] "` |  |
| email_use_tls | string | `"False"` |  |
| fullnameOverride | string | `"awx"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0] | string | `"chart-example.local"` |  |
| ingress.tls | list | `[]` |  |
| memcached.install | bool | `true` |  |
| metrics.annotations."prometheus.io/port" | string | `"9090"` |  |
| metrics.annotations."prometheus.io/scrape" | string | `"true"` |  |
| metrics.enabled | bool | `false` |  |
| metrics.port | int | `9419` |  |
| metrics.serviceMonitor.additionalLabels | object | `{}` |  |
| metrics.serviceMonitor.enabled | bool | `false` |  |
| metrics.serviceMonitor.honorLabels | bool | `false` |  |
| metrics.serviceMonitor.interval | string | `"30s"` |  |
| nodeSelector | object | `{}` |  |
| postgresql.image.registry | string | `"docker.io"` |  |
| postgresql.image.repository | string | `"bitnami/postgresql"` |  |
| postgresql.image.tag | float | `9.6` |  |
| postgresql.install | bool | `true` |  |
| postgresql.metrics.enabled | bool | `false` |  |
| postgresql.persistence.enabled | bool | `true` |  |
| postgresql.postgresqlDatabase | string | `"awx"` |  |
| postgresql.postgresqlPassword | string | `"awx"` |  |
| postgresql.postgresqlUsername | string | `"postgres"` |  |
| rabbitmq.install | bool | `true` |  |
| rabbitmq.rabbitmq.configuration | string | `"## Clustering\ncluster_formation.peer_discovery_backend  = rabbit_peer_discovery_k8s\ncluster_formation.k8s.host = kubernetes.default.svc.cluster.local\ncluster_formation.node_cleanup.interval = 10\ncluster_formation.node_cleanup.only_log_warning = false\ncluster_partition_handling = autoheal\n## queue master locator\nqueue_master_locator=min-masters\n## enable guest user\nloopback_users.guest = false\n## awx vhost\ndefault_vhost = awx"` |  |
| rabbitmq.rabbitmq.password | string | `"awx"` |  |
| rabbitmq.rabbitmq.username | string | `"awx"` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| server_email | string | `"root@localhost"` |  |
| service.externalPort | int | `8052` |  |
| service.internalPort | int | `8052` |  |
| tolerations | list | `[]` |  |
