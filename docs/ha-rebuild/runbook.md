# HA Cluster Rebuild Runbook

## Overview
Converting existing single-server k3s cluster (SQLite) to 3-server etcd HA cluster.

## Architecture
| Node | Role | OS | Storage | Arch |
|---|---|---|---|---|
| kali-raspberrypi | etcd server 1 | Kali Linux 2026.3 | SD+SSD | arm64 |
| pi2 | etcd server 2 | Ubuntu 26.04 | USB SSD | arm64 |
| Dell 7040 | etcd server 3 | Ubuntu 26.04 | Internal SSD | amd64 |
| multipass | worker | - | - | amd64 |

## Prerequisites
- kali-raspberrypi k3s data on SSD
- pi2 fresh Ubuntu 26.04 on USB SSD
- 7040 Ubuntu 26.04 on internal SSD
- All nodes reachable via SSH
- Cluster backup saved

## Phase 1 - Backup
## Phase 2 - Tear down existing cluster
## Phase 3 - Initialize etcd on kali-raspberrypi
## Phase 4 - Join pi2 as etcd server
## Phase 5 - Join 7040 as etcd server
## Phase 6 - Rejoin multipass as worker
## Phase 7 - Verify HA
## Phase 8 - Restore workloads
