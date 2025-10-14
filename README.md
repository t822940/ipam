# Deploy IPAM with Ansible

Simple Ansible playbook to deploy phpIPAM to Kubernetes.

## Setup

1. Install requirements:
   ```bash
   ansible-galaxy collection install -r requirements.yml
   pip install kubernetes
   ```

2. Deploy:
   ```bash
   ansible-playbook -i inventory playbook.yml
   ```

## Access

Access phpIPAM at: `http://<NODE_IP>:30080`

Get node IP: `kubectl get nodes -o wide`

## Cleanup

Remove: `kubectl delete namespace ipam`