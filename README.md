# Ansible Kong Example

> Examples for managing Kong services with Ansible

## Prerequisites

- Docker
- Ansible

## Usage

1. Spin up the stack
```bash
docker-compose up
```

2. Verify if Konga is running by going to http://localhost:1337

3. Run the playbook
```bash
ansible-playbook play.yml
```

4. Verify if the service was added via Konga or via the REST API
```bash
curl localhost:8001/services
```
