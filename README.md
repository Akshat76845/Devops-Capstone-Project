## QR-Based Production System

This is a production-ready QR-based system deployed with CI/CD, Docker,
and Kubernetes. It supports real-world use cases such as authentication,
payments, and tracking.

## Features
- QR code generation and validation
- Next.js frontend
- Backend API service
- CI/CD pipeline using GitHub Actions
- Containerized deployment with Docker
- Kubernetes manifests for production orchestration

## Tech Stack
- Frontend: Next.js
- Backend: Node.js / API service
- Containerization: Docker, Docker Compose
- Orchestration: Kubernetes
- CI/CD: GitHub Actions

## Architecture Overview
Frontend (Next.js) → Backend 
CI/CD → Docker Image → Kubernetes Deployment

## Running Locally
```bash
docker compose -f docker-compose.prod.yaml up
