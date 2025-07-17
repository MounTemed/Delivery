<div align="center">
    <h1>Delivery Project</h1>
    <h4></h4>
</div>


A sample Go web application to demonstrate a full CI/CD pipeline using Docker, Ansible, and GitHub Actions.

## 🚀 Tech Stack

*   **Application**: Go
*   **Containerization**: Docker & Docker Compose
*   **Configuration Management & Deployment**: Ansible
*   **CI/CD**: GitHub Actions

## 📂 Project Structure
```
.
├── ansible/ # Ansible playbooks for setup and deployment
├── .github/ # GitHub Actions workflows
├── images/ # Application source code and Dockerfile
└── compose.yaml # Docker Compose configuration for local run
```

## 🛠️ Usage

### Running Locally

1.  Clone the repository.
2.  Ensure you have Docker installed.
3.  Run the command:
  ```bash
  docker-compose up --build
  ```

4.  The application will be available at `http://localhost:8080`.

### Deployment

1.  Configure your servers in the inventory file `ansible/inventory/hosts.yaml`.
2.  Run the main deployment playbook:
  ```bash
  ansible-playbook ansible/playbook/delivery/master.yaml
  ```

## ⚙️ CI/CD

The CI/CD process is automated using GitHub Actions, defined in the `.github/workflows/cicd.yaml` file. On every push to the main branch, a Docker image is automatically built and subsequently deployed to the servers using Ansible.

## 📄 License

This project is distributed under the license specified in the [LICENSE](LICENSE) file.
