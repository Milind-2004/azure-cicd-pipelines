# Azure CI/CD Pipelines

Production-ready CI/CD pipeline templates for Azure DevOps and GitHub Actions.

## 📌 Overview
This repository contains pipeline templates for:
- Multi-stage build & release pipelines (Azure DevOps)
- SonarQube code quality integration
- GitHub Actions CI/CD workflows
- Automated deployment to Azure Web Apps

## 📁 Structure
```
├── azure-devops/
│   ├── build-pipeline.yml         # Build & artifact publishing
│   ├── release-pipeline.yml       # Multi-stage deployment (Dev → Staging → Prod)
│   └── sonarqube-integration.yml  # Static code analysis with quality gates
└── github-actions/
    ├── ci-workflow.yml            # Build, lint, test on push/PR
    └── deploy-to-azure.yml        # Deploy to Azure Web App on merge
```

## 🔐 Required Secrets
| Secret | Description |
|---|---|
| `AZURE_CREDENTIALS` | Azure service principal JSON |
| `AZURE_APP_NAME` | Target Azure Web App name |
| `SONAR_PROJECT_KEY` | SonarQube project key |

## 🚀 Pipeline Flow
```
Code Push → CI Build → SonarQube Analysis → Quality Gate → Deploy Dev → Staging → Prod
```

## 📜 License
MIT
