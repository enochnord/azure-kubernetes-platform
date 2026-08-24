# Target Platform Architecture

**Status:** Proposed
**Last reviewed:** 2026-08-17

## Overview

The Azure Kubernetes Platform is a learning-focused internal developer platform.
It will provide application teams with a standardized path for onboarding,
deploying, securing, observing, and operating containerized workloads.

The platform will begin locally with Docker and kind before extending into Azure
and AKS. Local development remains a supported path so that cloud access and
cost do not prevent platform development or testing.

## Target Workflow

```mermaid
flowchart TD
    A[Application team] --> B[Onboarding pull request]
    B --> C[Schema and policy validation]
    C --> D[Golden-path Helm chart]
    D --> E[GitOps desired state]
    E --> F[Argo CD reconciliation]
    F --> G[Kubernetes workload]
    G --> H[Prometheus metrics]
    H --> I[Grafana dashboards and alerts]
    J[Bicep Azure foundation] --> G