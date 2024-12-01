# HashiCorp Infrastructure Management Cluster Terraform Setup

## Prerequisites
- Proxmox VE installed
- Terraform 1.5+ installed
- HashiCorp Consul, Nomad, and Vault downloaded
- Network VLAN configured

## Configuration Steps

1. Clone the repository
2. Create `terraform.tfvars` with:
```hcl
proxmox_api_url = "https://your-proxmox-url:8006/api2/json"
proxmox_api_token_id = "your-token-id"
proxmox_api_token_secret = "your-secret-token"
```

3. Initialize Terraform:
```bash
terraform init
```

4. Validate configuration:
```bash
terraform plan
```

5. Apply configuration:
```bash
terraform apply
```

## Security Recommendations
- Use Vault for secrets management
- Enable Full Disk Encryption
- Implement strict firewall rules
- Rotate credentials regularly

## Cluster Components
- 3 Consul Servers
- 3 Nomad Servers
- 3 Vault Servers
- Dedicated Infrastructure VLAN

## Networking
- VLAN: 10
- Subnet: 10.0.10.0/24
- Gateway: 10.0.10.1

## Monitoring
- Prometheus metrics enabled
- Syslog integration
- Audit logging for Vault