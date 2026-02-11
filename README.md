# QR Code Platform — Production-Ready Full-Stack System

This is a production-ready QR-based system deployed with CI/CD, Docker, and Kubernetes.
It supports real-world use cases like authentication, device linking, and tracking.

## What this system does
Users can scan a QR code to authenticate or link devices.
The Next.js frontend displays QR codes and user state.
The Node.js API validates scans and manages sessions.

This architecture is designed to be used in SaaS platforms, event check-ins,
payment terminals, or IoT device onboarding.

## Architecture
- Frontend: Next.js
- Backend: Node.js REST API
- Containers: Docker
- CI/CD: GitHub Actions
- Orchestration: Kubernetes
- Production deployment: docker-compose.prod.yaml

Frontend → API → Database  
CI/CD → Docker → Kubernetes

## Why this exists
This project demonstrates how to build and deploy a real production system
from source code to Kubernetes with automated pipelines.

It is designed to show skills in:
- Full-stack development
- DevOps & CI/CD
- Containerized production deployments
- Kubernetes orchestration

## Run locally
```bash
docker compose -f docker-compose-prod.yaml up
