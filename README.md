
# README.md

## Project Setup & Commands

### Docker & Docker Compose Commands

| Command | Purpose |
|---------|---------|
| `docker-compose up` | Build and start all microservices defined in docker-compose.yml |
| `docker-compose down` | Stop and remove all running containers |
| `docker-compose build` | Build Docker images for all services without starting them |
| `docker ps` | List all running containers |
| `docker logs <container-id>` | View logs from a specific container |

### GitHub Actions Commands

| Command | Purpose |
|---------|---------|
| `git push origin main` | Trigger the CI/CD pipeline by pushing code changes to the main branch |
| GitHub Actions Auto-Build | Automatically builds and pushes Docker images for all services on main branch push |

### Service Ports

- API Gateway: `http://localhost:4000`
- Auth Service: `http://localhost:4001`
- Patient Service: `http://localhost:4002`
- Doctor Service: `http://localhost:4003`
- Appointment Service: `http://localhost:4004`
- Notification Service: `http://localhost:4005`

### Prerequisites

- Docker & Docker Compose installed
- Docker Hub credentials configured in GitHub Secrets (`DOCKER_USERNAME`, `DOCKER_PASSWORD`)
