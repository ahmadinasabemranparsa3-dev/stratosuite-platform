# StratoSuite Platform

StratoSuite Platform is a cloud-native, modular technical portfolio ecosystem designed to demonstrate production-grade serverless architecture using AWS managed services.

This platform consists of multiple independently deployed full-stack applications operating under a unified infrastructure and authentication system.

---

## Architecture Overview

StratoSuite follows a serverless, microservices-inspired architecture:

Frontend:
- React applications
- Hosted on Amazon S3
- Delivered globally via Amazon CloudFront (single distribution with path-based routing)

Backend:
- AWS Lambda (Node.js runtime)
- Amazon API Gateway (REST APIs)
- Amazon DynamoDB (NoSQL database)

Infrastructure:
- Serverless Framework
- AWS CloudFormation (via Serverless)

Authentication:
- Centralized JWT-based authentication service
- Shared across all modules

---

## Platform Modules

The platform includes the following applications:

- Pro-Tasker – Advanced productivity and task management
- NoteNest – Structured note-taking system
- Flashcard App – Learning reinforcement tool
- Kanban Task Management App – Board-based workflow system
- In-Browser Markdown Editor – Lightweight documentation system

Each module:
- Is independently deployed
- Owns its own backend service
- Owns its own DynamoDB tables
- Shares centralized authentication
- Is routed through a unified CloudFront distribution

---

## Cloud Design Principles

- Fully serverless architecture
- Infrastructure as Code
- Service isolation per module
- User-scoped data access
- Path-based CDN routing
- Scalable and production-oriented design

---

## Deployment Model

Frontend:
React build → S3 → CloudFront

Backend:
API Gateway → Lambda → DynamoDB

Authentication:
Dedicated auth service issuing JWT tokens used across all modules

---

## Purpose

This project demonstrates:
- Cloud architecture design
- Serverless backend engineering
- NoSQL data modeling
- Modular system design
- Production-level AWS service integration

StratoSuite Platform is designed to represent a real-world SaaS ecosystem rather than standalone demo applications.
