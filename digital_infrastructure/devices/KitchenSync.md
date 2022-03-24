---
layout: default
title: KitchenSync
parent: Devices
grand_parent: Digital Infrastructure
nav_order: 4
---

# KitchenSync

| Attribute              | Value                                                        | Notes                                   |
| ---------------------- | ------------------------------------------------------------ | --------------------------------------- |
| Location               | Workshop>Network Cabinet                                     |                                         |
| Internal hostname      | kitchensync.local                                            |                                         |
| External hostname      | members.unit1.farsetlabs.org.uk                              |                                         |
| External port forwards | SSH, DSM Web Station, HTTP(S), and [MQTT](../services/MQTT.md) (regular + websocket) | MQTT passed through to docker container |

KitchenSync is a Synology DS1511+ 5-bay NAS (currently only populated with 3x4TB WD40 disks)

It is a shared storage server that also serves as our primary onsite [Docker](../services/Docker.md) server and SSH jumpbox

## Getting Access

If you want access to KitchenSync, fire an email to tech@farsetlabs.org.uk and we'll set you up with a (quotaed) account.

