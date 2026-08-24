# Azure Kubernetes Platform

A hands-on platform engineering capstone that builds a small internal developer
platform for onboarding, deploying, securing, observing, and operating
containerized services.

## Project Goal

Enable an application team to submit a small, reviewable onboarding
configuration and receive a standardized, secure, and observable deployment
without designing its Kubernetes and delivery stack from scratch.

## Current Status

**Week 1, Day 1:** Local development environment and platform definition.

Currently implemented:

- WSL 2 development environment
- Docker Desktop with WSL integration
- Platform charter
- Target architecture

The application and platform capabilities will be added incrementally. Features
described as target architecture should not be interpreted as currently
implemented.

## Planned Golden Path

A developer will eventually be able to:

1. Define a service through a small onboarding configuration.
2. Receive automated schema, manifest, and policy feedback.
3. Deploy through a reusable Helm workload standard.
4. Promote an immutable artifact through reviewed environment changes.
5. Receive health checks, security controls, metrics, dashboards, and runbooks.
6. Rely on Argo CD to reconcile the declared state.

## Technology Roadmap

- Docker and Docker Compose
- Kubernetes with kind
- Helm
- GitHub Actions
- Azure Kubernetes Service and Azure Container Registry
- Bicep
- Microsoft Entra Workload ID and Key Vault
- Prometheus, Grafana, Alertmanager, and OpenTelemetry
- Kyverno
- Argo CD

Tools are introduced only when they satisfy a demonstrated platform requirement.

## Repository Structure

```text
azure-kubernetes-platform/
├── apps/                       # Reference API and worker
├── platform/                   # Golden path, catalog, and environments
├── infrastructure/bicep/       # Azure infrastructure
├── policies/kyverno/           # Policy-as-code guardrails
├── observability/              # Metrics, dashboards, alerts, and SLOs
├── gitops/argocd/              # GitOps reconciliation
├── docs/                       # Architecture, decisions, onboarding, runbooks
└── .github/workflows/          # Continuous integration and delivery