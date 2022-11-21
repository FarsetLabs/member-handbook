---
layout: default
title: KitchenSync
parent: Devices
grand_parent: Digital Infrastructure
nav_order: 4
---

# KitchenSync

| Attribute              | Value                                                                                | Notes                                   |
| ---------------------- | ------------------------------------------------------------------------------------ | --------------------------------------- |
| Location               | Workshop>Network Cabinet                                                             |                                         |
| Internal hostname      | kitchensync.local                                                                    |                                         |
| External hostname      | members.unit1.farsetlabs.org.uk                                                      |                                         |
| External port forwards | SSH, DSM Web Station, HTTP(S), and [MQTT](../services/MQTT.md) (regular + websocket) | MQTT passed through to docker container |

KitchenSync is a Synology DS1511+ 5-bay NAS (currently only populated with 3x4TB WD40 disks)

It is a shared storage server that also serves as our primary onsite [Docker](../services/Docker.md) server and SSH jumpbox

## Application Portal

KitchenSync also serves as a reverse proxy for the following services; 

| External URL                 | Service                           | Internal URL             |
| ---------------------------- | --------------------------------- | ------------------------ |
| https://ha.farsetlabs.org.uk | [HomeAssistant](homeassistant.md) | homeassistant.local:8123 |


### Adding additional reverse proxies

Any desired external URL **not** under *.members.unit1.farsetlabs.org.uk will require an additional entry in [Route53](../services/Route53.md)) to redirect the desired URL as an A record Alias to `members.unit1.farsetlabs.org.uk`

Additionally, if HTTPS is required, a Lets Encrypt certificate can be generated on the relevant subdomain, and assigned to the portal, via "Control Panel" > "Security" > "Certificates"

For many interactive services, you may need to enable Websockets Custom Headers in the Reverse Proxy configuration (through the 'Create' button on the relevant tab)

## Getting Access

If you want access to KitchenSync, fire an email to tech@farsetlabs.org.uk and we'll set you up with a (quotaed) account.
