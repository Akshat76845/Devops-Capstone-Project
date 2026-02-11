
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
=======
# devops-qr-code

This is the sample application for the DevOps Capstone Project.
It generates QR Codes for the provided URL, the front-end is in NextJS and the API is written in Python using FastAPI.

## Application

**Front-End** - A web application where users can submit URLs.

**API**: API that receives URLs and generates QR codes. The API stores the QR codes in cloud storage(AWS S3 Bucket).

## Running locally

### API

The API code exists in the `api` directory. You can run the API server locally:

- Clone this repo
- Make sure you are in the `api` directory
- Create a virtualenv by typing in the following command: `python -m venv .venv`
- Install the required packages: `pip install -r requirements.txt`
- Create a `.env` file, and add you AWS Access and Secret key, check  `.env.example`
- Also, change the BUCKET_NAME to your S3 bucket name in `main.py`
- Run the API server: `uvicorn main:app --reload`
- Your API Server should be running on port `http://localhost:8000`

### Front-end

The front-end code exits in the `front-end-nextjs` directory. You can run the front-end server locally:

- Clone this repo
- Make sure you are in the `front-end-nextjs` directory
- Install the dependencies: `npm install`
- Run the NextJS Server: `npm run dev`
- Your Front-end Server should be running on `http://localhost:3000`


## Goal

The goal is to get hands-on with DevOps practices like Containerization, CICD and monitoring.

Look at the capstone project for more detials.

## Author

[Rishab Kumar](https://github.com/rishabkumar7)

## License

[MIT](./LICENSE)
(Production docker-compose and deployment setup)
