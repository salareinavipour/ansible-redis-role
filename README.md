# Redis-Sentinel

A production-grade, high-available Redis deployment using Sentinel and Keepalived.


## Role Variables

### Redis Variables

| Variable | Description | Default Value |
| --- | --- | --- |
| redis__image     | | "bitnami/redis" |
| redis__image_tag | | "6.2" |
| redis__path      | | "/opt/redis" |
| redis__port      | |  6379 | 
| redis__user      | |  "redis" |
| redis__password  | | "redis" |
| redis__master_password | | "redis" |
| redis__exporter_image | | "bitnami/redis-exporter" |
| redis__exporter_image_tag | | "1" |

### Sentinel Variables

| Variable | Description | Default Value |
| --- | --- | --- |
| redis__sentinel_image     | | "bitnami/redis-sentinel" |
| redis__sentinel_image_tag | | "6.2" |
| redis__sentinel_reset     | | False |
| redis__sentinel_failover_timeout        | | "30000" |
| redis__sentinel_down_after_milliseconds | | "30000" |

### Keepalived Variables

| Variable | Description | Default Value |
| --- | --- | --- |
| redis__docker_keepalived_image     | | "quay.io/salareinavi/keepalived-redis" |
| redis__docker_keepalived_image_tag | | "v0.1" |
| redis__keepalived_auth_pass        | | "redis" |
| redis__private_interface           | | eth0 |
| redis__virtual_router_id           | | "51" |
