
# 🚀 CI/CD Flask Application

**Version:** `1.0.7`

A containerized Flask application demonstrating a CI/CD pipeline using Docker, GitHub Actions, and Semantic Versioning.

---

## 📌 Overview

This project demonstrates an automated software delivery workflow, including Docker image builds, application health checks, version tagging, and publishing images to Docker Hub.

## 🛠️ Key Features

- ⚙️ Automated CI/CD using GitHub Actions
- 🐳 Docker image build and publishing
- 🏷️ Semantic Versioning using Git tags
- ❤️ Automated health check validation
- 📦 Docker Hub integration
- 🔄 Automated release workflow

## 🔄 CI/CD Workflow

1. Push a Git tag (e.g., `v1.0.0`).
2. GitHub Actions triggers the pipeline.
3. The Docker image is built.
4. A container is started and validated using `/health`.
5. The image is tagged with its version and `latest`.
6. The image is pushed to Docker Hub.

## 🌐 Application Endpoints

| Endpoint | Description |
|---|---|
| `/` | Displays application status and version |
| `/health` | Health check endpoint returning HTTP 200 |

## 🧰 Tech Stack

- **Application:** Python, Flask
- **Containerization:** Docker
- **CI/CD:** GitHub Actions
- **Version Control:** Git
- **Scripting:** Bash, Linux
- **Versioning:** Semantic Versioning (SemVer)

## 🚀 Run Locally with Docker

### 1. Clone the repository

```bash
git clone https://github.com/talkeret1/ci-cd-flask-app.git
cd ci-cd-flask-app
```

### 2. Build the image

```bash
docker build -t ci-cd-flask-app .
```

### 3. Run the container

```bash
docker run -d --name flask-app -p 5000:5000 ci-cd-flask-app
```

### 4. Verify the application

- Application: http://localhost:5000/
- Health check: http://localhost:5000/health

Or run:

```bash
curl -i http://localhost:5000/health
```

> 💡 The example assumes the application listens on port `5000` inside the container.

## 🏷️ Versioning

The project follows Semantic Versioning:

`MAJOR.MINOR.PATCH`

To trigger a release:

```bash
git tag v1.0.0
git push origin v1.0.0
```

## 🔐 Configuration

Docker Hub credentials should be stored securely as GitHub Actions repository secrets:

- `DOCKERHUB_USERNAME`
- `DOCKERHUB_TOKEN`

Never commit sensitive credentials to the repository.

## 🔭 Future Improvements

- Terraform for Infrastructure as Code
- Kubernetes for container orchestration
- AWS cloud deployment
- Automated security scanning and monitoring

## 🔗 Links

- **GitHub:** https://github.com/talkeret1/ci-cd-flask-app
- **LinkedIn:** https://www.linkedin.com/in/talkeret

---

**DevOps · Docker · CI/CD Automation · Infrastructure as Code**
