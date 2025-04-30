# Yii2 Application Deployment on AWS EC2 via Docker Swarm + Ansible + GitHub Actions

## Steps:

1. Launch Ubuntu 22.04 EC2 Instance
2. Allow 22, 80, 8080 in Security Group
3. Add SSH Key to GitHub Secrets
4. Configure Ansible inventory and run:

```bash
ansible-playbook -i inventory ansible/playbook.yml
```

5. Push Code to `main` branch → Automatic CI/CD

## Secrets Required:

- DOCKER_USERNAME
- DOCKER_PASSWORD
- SERVER_IP
- SERVER_USER
- SERVER_SSH_KEY (private key)

## Check:

Visit: `http://<your-ec2-public-ip>`
