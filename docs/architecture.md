# System Architecture

## Overview
DevOps Simulator follows a **microservices architecture** designed for high availability and scalability.

**Development Version**: Includes local development setup with hot reload.  
**Experimental Version**: Adds AI/ML integration, multi-cloud orchestration, and chaos engineering features.

## Core Components

### 1. Application Server
- **Technology**: Node.js + Express (+ TensorFlow.js for experimental)
- **Ports**: 
  - Development: 3000  
  - Experimental: 9000 (main), 9001 (metrics), 9002 (AI API)
- **Scaling**: Manual in development, AI-powered predictive auto-scaling in experimental
- **Debug/Intelligence**: Chrome DevTools debugger for dev, real-time ML inference for experimental
- **Message Queue**: Apache Kafka (experimental)

### 2. Database Layer
- **Development**: Local PostgreSQL 14, single instance, auto-seeded
- **Experimental**: PostgreSQL 14 cluster (5 nodes), multi-master replication, Redis cluster with ML cache optimization
- **Backup**: Manual for dev, continuous with geo-redundancy for experimental
- **AI Features**: Query optimization, index suggestions (experimental)

### 3. Monitoring & Observability
- **Development**: Console logging, Prometheus optional
- **Experimental**: Prometheus + Thanos, ELK stack, AI log analysis
- **Alerts**: Console warnings in dev, advanced anomaly detection in experimental

### 4. Container Orchestration
- **Development**: Docker Compose with hot reload
- **Experimental**: Kubernetes with custom CRDs, global anycast load balancing, cross-cloud failover

### 5. Authentication
- **Development**: OAuth2 + JWT, Redis sessions
- **Experimental**: OAuth2, AI-powered security analysis, multi-cloud authentication integration

## Deployment Strategy
- **Development**: Docker Compose hot reload, rollback via Git checkout
- **Experimental**: Automated cross-cloud deployment with zero-downtime failover

## Security
- **Development**: SSL/TLS disabled, CORS enabled, debug endpoints exposed
- **Experimental**: Zero-trust, AES-256 encryption, comprehensive audit logging

## Workflow
1. Make code changes
2. Auto-reload triggers rebuild (dev)
3. Run unit tests
4. Check console logs
5. Commit when ready

## Experimental Features
- Multi-cloud deployment
- AI-powered log analysis
- Automatic rollback on anomaly detection
- Predictive auto-scaling
- Chaos engineering
