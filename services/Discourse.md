---
layout: default
title: Discourse
parent: Services
nav_order: 1
---

# Discourse

Discourse is our Forum platform, for longer term discussions and project documentation

It is running on an [Azure](../environments/Azure.md) VM

It previously ran as a [Bitnami](https://docs.bitnami.com/azure/apps/discourse/) stack, but that was poorly documented, unstable, and generally unmanagable

This service *could* be migrated to a Dockerised version but the resource requirements for running Discourse made running it in our [KitchenSync](../devices/KitchenSync.md) based [Docker](../services/Docker.md) environment infeasable.

## Build/Edit log

* Killed old discourse VM's/Disks/IP's from Azure, 
* Spun up new blank Ubuntu LTS image on D1v2
* Used SSHkey from `bolster` account on Kitchensync as base key ID
* Followed [these](https://github.com/discourse/discourse/blob/master/docs/INSTALL-cloud.md) instructions, using the sendgrid as the SMTP relay
* Configured Google OAuth under bolster@farsetlabs.org.uk -> Discourse project
* Added [solved](https://github.com/discourse/discourse-solved), [assign](https://github.com/discourse/discourse-assign) [voting](https://github.com/discourse/discourse-voting), and [user-notes](https://github.com/discourse/discourse-user-notes) plugins
* Set @farsetlabs.org.uk emails to automatically be trusted
* Setup Unattended Upgrades and fail2ban
