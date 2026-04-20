# Cloud SDLC Pipeline

**A Cloud TPM's CI/CD orchestration framework for cloud-native applications — covering pipeline design, infrastructure as code, security gates, deployment strategies, and rollback procedures.**

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?style=flat-square&logo=amazonaws)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Role](https://img.shields.io/badge/Role-Cloud%20TPM-blue?style=flat-square)

---

## Project Overview

This repository documents a production-grade CI/CD pipeline framework for cloud-native applications on AWS. It reflects real-world TPM leadership in aligning engineering, security, and operations teams around a unified software delivery lifecycle — from code commit to production deployment with automated quality and security gates at every stage.

**Business Context:** The organization's deployment process was manual, error-prone, and slow — averaging 2-week release cycles with a 15% rollback rate. This pipeline framework reduced deployment lead time to under 30 minutes, cut rollback rates to less than 2%, and established automated security scanning that caught 94% of vulnerabilities before production.

---

## Repository Structure

cloud-sdlc-pipeline/
|-- ci-cd/              # Pipeline definitions, build configs, and deployment workflows
|-- iac/                # Terraform modules, CloudFormation templates, and IaC configs
|-- security-gates/     # SAST/DAST configs, vulnerability scanning, and compliance checks
|-- deployment/         # Blue/green deployment configs, canary release strategies
|-- rollback/           # Rollback procedures, automated recovery scripts
|-- README.md

---

## TPM Delivery Framework

| Phase | Description | Key Activities | Quality Gate |
|-------|-------------|---------------|-------------|
| Plan & Design | Requirements gathering and architecture review | Story mapping, tech design docs, dependency analysis | Architecture review approved |
| Build & Test | Code development with automated testing | Unit tests, integration tests, code coverage enforcement | 90%+ code coverage |
| Security Scan | Automated vulnerability and compliance checks | SAST, DAST, dependency scanning, license checks | Zero critical/high findings |
| Deploy | Automated deployment with progressive rollout | Blue/green deployment, canary analysis, traffic shifting | Health checks passing |
| Monitor & Validate | Post-deployment verification and observability | Synthetic monitoring, error rate tracking, performance baselines | SLA metrics within threshold |

---

## Key Results

| Metric | Before | After | Impact |
|--------|--------|-------|--------|
| Deployment Lead Time | 2 weeks | Under 30 min | **95% faster delivery** |
| Deployment Frequency | Biweekly | Multiple daily | **10x throughput** |
| Rollback Rate | 15% | Under 2% | **87% fewer failures** |
| Vulnerability Escape Rate | 30%+ to prod | Under 6% | **94% pre-prod catch rate** |
| Change Failure Rate | 20% | Under 5% | **4x reliability improvement** |

---

## Domain Breakdown

### `/ci-cd` — Pipeline Configuration
- CodePipeline and CodeBuild buildspec definitions
- Multi-stage pipeline architecture (dev, staging, prod)
- Artifact management and versioning strategy
- Pipeline-as-code templates for rapid onboarding of new services

### `/iac` — Infrastructure as Code
- Terraform modules for VPC, ECS, RDS, and supporting infrastructure
- CloudFormation templates for environment provisioning
- State management and backend configuration
- Module versioning and dependency management patterns

### `/security-gates` — Security & Compliance Automation
- SAST integration with CodeBuild (SonarQube, Semgrep)
- DAST scanning configuration for staging environments
- Dependency vulnerability scanning (Snyk, Dependabot)
- License compliance checks and policy enforcement

### `/deployment` — Deployment Strategies
- Blue/green deployment configuration with ALB target group switching
- Canary release automation with CloudWatch-based analysis
- Traffic shifting policies and rollout percentage schedules
- Feature flag integration for controlled feature releases

### `/rollback` — Recovery & Rollback
- Automated rollback triggers based on error rate and latency thresholds
- One-click rollback procedures via CodeDeploy
- Database migration rollback strategies and data integrity checks
- Post-rollback validation checklists and incident documentation

---

## DORA Metrics Dashboard

| DORA Metric | Target | Achieved | Rating |
|-------------|--------|----------|--------|
| Deployment Frequency | Multiple daily | 4-6 per day | **Elite** |
| Lead Time for Changes | Under 1 hour | ~30 minutes | **Elite** |
| Change Failure Rate | Under 5% | 3.2% | **Elite** |
| Time to Restore Service | Under 1 hour | ~25 minutes | **Elite** |

---

## Tools & Services

| Category | Tools |
|----------|-------|
| **AWS Services** | CodePipeline, CodeBuild, CodeDeploy, ECR, ECS, Lambda, S3 |
| **Infrastructure as Code** | Terraform, CloudFormation |
| **Security Scanning** | SonarQube, Semgrep, Snyk, OWASP ZAP |
| **Monitoring** | CloudWatch, X-Ray, Datadog |
| **Program Management** | Jira, Confluence, GitHub Actions |

---

## TPM Lens — Program Management Perspective

This project demonstrates core Cloud TPM competencies:

- **SDLC Orchestration:** Designed end-to-end pipeline architecture aligning 4 engineering teams on shared deployment standards, branching strategies, and release cadence
- **Security Integration:** Embedded security gates into the CI/CD pipeline — shifting security left without slowing delivery velocity
- **Metrics-Driven Culture:** Established DORA metrics tracking that provided engineering leadership with real-time visibility into delivery performance
- **Risk Mitigation:** Built automated rollback capabilities that reduced mean time to recovery from hours to minutes — protecting customer experience during failed deployments
- **Developer Experience:** Reduced onboarding time for new services from 2 weeks to 2 days through reusable pipeline templates and self-service IaC modules

---

## Lessons Learned

- **Shift-left security works:** Catching vulnerabilities in CI is 10x cheaper than in production — invest in scanning early
- **Progressive rollouts reduce blast radius:** Canary deployments caught 3 critical issues that would have impacted 100% of users
- **Pipeline-as-code enables scale:** Templated pipelines let teams self-serve without platform team bottlenecks
- **Rollback confidence enables velocity:** Teams deploy more frequently when they trust the rollback mechanism

---

## Related Projects

| Project | Description |
|---------|-------------|
| [Cloud Migration Architecture](https://github.com/Ewuack/cloud-migration-architecture) | On-prem to AWS migration program |
| [HIPAA Cloud Governance Framework](https://github.com/Ewuack/hipaa-cloud-governance-framework) | Compliance-as-code for regulated environments |
| [AWS Cost Optimization Playbook](https://github.com/Ewuack/aws-cost-optimization-playbook) | Strategic cost reduction across AWS infrastructure |
| [Cloud Incident Response Simulation](https://github.com/Ewuack/cloud-incident-response-simulation) | Security incident detection and response |

---

**Author:** Erick Guacamaya — Cloud Technical Program Manager
**LinkedIn:** [linkedin.com/in/erickguacamaya](https://linkedin.com/in/erickguacamaya) | **GitHub:** [github.com/Ewuack](https://github.com/Ewuack)
