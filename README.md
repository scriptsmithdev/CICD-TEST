# DevSecOps2026-GHA

A DevSecOps project using GitHub Actions (GHA) for CI/CD pipeline automation with Docker.

## Project Structure

```
.
├── .github/workflows/   # GitHub Actions workflow definitions
├── css/                 # Stylesheets
├── images/              # Static images
├── Dockerfile           # Docker image definition
├── index.html           # Main HTML page
└── ascii-script.sh      # ASCII art script
```

## Workflows

| Workflow | Trigger | Description |
|---|---|---|
| `test.yml` | Push to `main`, `feature/*` | Builds Docker image |
| `first_workflow.yml` | - | Introductory workflow |
| `multiple-jobs.yml` | - | Multi-job pipeline demo |
| `ascii-workflow.yml` | - | ASCII script workflow |

## Getting Started

### Prerequisites
- Docker
- GitHub account with Actions enabled

### Run Locally

```bash
docker build -t devsecops2026 .
docker run -p 80:80 devsecops2026
```

## CI/CD Pipeline

Pushes to `main` or `feature/*` branches trigger the Docker build workflow. Changes to `.gitignore`, `README.md`, or workflow files are excluded from triggering builds.
