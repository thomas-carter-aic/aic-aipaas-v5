aic-aipaas-v5
Overview
aic-aipaas- is an AI-native PaaS/SaaS/AI PaaS platform designed to:

Enable SMB clients (small and medium businesses) to self-serve AI solutions, maximizing ROI for business goals, processes, and operations through intuitive interfaces, prebuilt AI templates (e.g., sales forecasting, customer segmentation, chatbots, inventory optimization), and integrations with SMB tools (Shopify, QuickBooks, HubSpot).
Enhance AI consultancy operations through efficient client management, analytics (client adoption, revenue, retention), and automation.
Support advanced features like quantum computing preparation (Qiskit), a full blockchain-based marketplace (Hyperledger Fabric), and generative AI agents (e.g., customer support chatbots, content generation).

The platform uses a polyglot microservices architecture (Java, Python, Go, Rust, TypeScript) with clean/hexagonal architecture, CQRS, sagas, Bazel-managed monorepo, REST/GraphQL APIs, database-agnostic (PostgreSQL, MongoDB, ClickHouse), and cloud-agnostic (AWS EKS, on-premises) deployments. It leverages FOSS tools (Spring Boot, FastAPI, NestJS, Keycloak, Strapi, Medusa) and aligns with 15-Factor App and MACH principles for a 20-year competitive moat.
Repository Structure

/apps/services/: Microservices (e.g., model-service, inference-service, marketplace-service).
/apps/microfrontends/: Next.js/TypeScript microfrontends (e.g., shell, model-mfe, user-mfe).
/packages/: Shared libraries and SDKs (e.g., plugin-sdk, blockchain, quantum).
/docs/: Documentation (requirements, architecture, design, testing).
/infrastructure/: Kubernetes, Helm, Docker, and blockchain/quantum configurations.
/ci-cd/: GitHub Actions, ArgoCD, Tekton pipelines.
/scripts/: Build, deploy, and scaffolding scripts.
/tools/: CMS (Strapi), mock services, sandbox.

Getting Started

Clone the repository: git clone https://github.com/thomas-carter-aic/aic-aipaas-v5.git
Run the scaffolding script: ./scripts/scaffold_aic_aipaas.sh
Set up environment: Configure /infrastructure/docker/docker-compose.yml for local development.
Install dependencies: Follow service-specific instructions (e.g., pom.xml, requirements.txt, package.json).

Development Workflow

Make small, incremental changes.
Write and run tests (/tests/ for each service).
Commit and push changes after tests pass.
Use pull requests with code reviews for the main branch.

License
MIT License (see /LICENSE).
