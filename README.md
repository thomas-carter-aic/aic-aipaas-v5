# aic-aipaas-v5

## Overview
aic-aipaas- is an AI-native PaaS/SaaS/AI PaaS platform designed to:

aic-aipaas is an AI-native PaaS/SaaS/AI PaaS platform designed to:

* Enable aand empower SMB clients with self-service AI tools and solutions to 
  maximize ROI in business processes, business goals, processes, and operations
  through intuitive interfaces, prebuilt AI templates (e.g., sales forecasting, 
  customer segmentation, chatbots, inventory optimization), and integrations 
  with SMB tools (Shopify, QuickBooks, HubSpot, etc.) while enhancing AI consultancy 
  operations through efficient client management, analytics, and automation.

* Prepare for support of advanced features like quantum computing preparation 
  (Qiskit), a full blockchain-based marketplace (Hyperledger Fabric), and generative 
  AI agents (e.g., customer support chatbots, content generation).

The platform uses a polyglot microservices architecture (Java, Python, Go, Rust, 
TypeScript) with clean/hexagonal architecture, CQRS, sagas, Bazel-managed monorepo, 
REST/GraphQL APIs, database-agnostic (PostgreSQL, MongoDB, ClickHouse), and cloud-agnostic 
(AWS EKS, on-premises) deployments. It leverages FOSS tools including Spring Boot, 
FastAPI, NestJS, Keycloak, Strapi, Medusa, etc. and aligns with 15-Factor App and MACH 
principles for a 20-year competitive moat.


## Key Features

* Self-service AI model deployment and inference for SMBs.
* Data integration with SMB tools (Shopify, QuickBooks, HubSpot).
* Marketplace for plugins and integrations.
* User, admin, developer, support, investor, marketing, low-code, and partner portals.
* Multi-tenant SaaS with billing, payments, and engagement.
* Governance, identity, inventory, and workspace management.
* FOSS stack with Bazel-managed monorepo.


## Repository Structure

* /apps/services/: Microservices (e.g., model-service, inference-service, marketplace-service).
* /apps/microfrontends/: Next.js/TypeScript microfrontends (e.g., shell, model-mfe, user-mfe).
* /packages/: Shared libraries and SDKs (e.g., plugin-sdk, blockchain, quantum).
* /docs/: Documentation (requirements, architecture, design, testing).
* /infrastructure/: Kubernetes, Helm, Docker, and blockchain/quantum configurations.
* /ci-cd/: GitHub Actions, ArgoCD, Tekton pipelines.
* /scripts/: Build, deploy, and scaffolding scripts.
* /tools/: CMS (Strapi), mock services, sandbox.


## Getting Started

1. Clone the repository.
2. Run `./scripts/scaffold_aic_aipaas.sh` to initialize structure.
3. Install dependencies (e.g., Bazel, Docker).
4. Set up environment: Configure `/infrastructure/docker/docker-compose.yml` for local development.
5. Install dependencies: Follow service-specific instructions (e.g., pom.xml, requirements.txt, package.json).
6. Run `docker compose up -d` for local environment.
7. Build with `bazel build //....`


## Development Workflow

 - Make small, incremental changes.
 - Write and run tests (/tests/ for each service).
 - Commit and push changes after tests pass.
 - Use pull requests with code reviews for the main branch.
 - Use feature branches and PRs.
 - Test with bazel test //....
 - Lint with language-specific tools.

## License
MIT License (see /LICENSE).
