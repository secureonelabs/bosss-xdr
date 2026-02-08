<!---
Copyright (C) 2015, Wazuh Inc.
Created by Wazuh, Inc. <info@wazuh.com>.
This program is free software; you can redistribute it and/or modify it under the terms of GPLv2
-->

# Centralized Configuration
## Index
- [Centralized Configuration](#centralized-configuration)
  - [Index](#index)
  - [Purpose](#purpose)
  - [Sequence diagram](#sequence-diagram)

## Purpose

One of the key features of Wazuh as a EDR is the Centralized Configuration, allowing to deploy configurations, policies, rootcheck descriptions or any other file from BOSSS XDR Manager to any BOSSS XDR Agent based on their grouping configuration. This feature has multiples actors: BOSSS XDR Cluster (Master and Worker nodes), with `wazuh-remoted` as the main responsible from the managment side, and BOSSS XDR Agent with `wazuh-agentd` as resposible from the client side.


## Sequence diagram
Sequence diagram shows the basic flow of Centralized Configuration based on the configuration provided. There are mainly three stages:
1. BOSSS XDR Manager Master Node (`wazuh-remoted`) creates every `remoted.shared_reload` (internal) seconds the files that need to be synchronized with the agents.
2. BOSSS XDR Cluster as a whole (via `wazuh-clusterd`) continuously synchronize files between BOSSS XDR Manager Master Node and BOSSS XDR Manager Worker Nodes
3. BOSSS XDR Agent `wazuh-agentd` (via ) sends every `notify_time` (ossec.conf) their status, being `merged.mg` hash part of it. BOSSS XDR Manager Worker Node (`wazuh-remoted`) will check if agent's `merged.mg` is out-of-date, and in case this is true, the new `merged.mg` will be pushed to BOSSS XDR Agent.