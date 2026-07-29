# DevOps Homelab

## Architecture
- **HA k3s cluster** (3 etcd servers): Raspberry Pi 5, Raspberry Pi 4, Dell OptiPlex 7040
- **Worker node**: multipass VM on Intel MacBook
- **Local cloud emulator**: Floci on Dell OptiPlex 7040 (70+ AWS services)
- **Mixed architecture**: arm64 (Pis) + amd64 (7040, MacBook)


## Stack
- Kubernetes: k3s v1.35.5
- Container runtime: containerd
- Ingress: Traefik
- Storage: Longhorn (planned)
- IaC: Terraform
- Local AZ (azure) emulation: Floci 1.5.33
