# PulseWatch

An uptime monitoring and public status page platform, built as a hands-on DevSecOps project on AWS.

**Status:** Work in progress (planning phase).

## Goals
- Practice DevSecOps end to end: containers, infrastructure as code, CI/CD with security gates, Kubernetes and observability.
- Stay production-minded: least privilege, no secrets in code, repeatable deployments, documented decisions.

## Planned services
| Service | Purpose |
|---|---|
| api-service | Authentication, monitor management, multi-tenancy |
| scheduler | Finds due monitors and enqueues checks |
| checker-workers | Run HTTP, TCP and SSL checks |
| alert-service | Deduplicates and sends notifications |

## Planned layout
```
services/     application code
infra/        Terraform
deploy/       Helm charts and GitOps config
workstation/  bootstrap scripts for the dev machine
docs/         architecture, decisions, runbooks, postmortems
```
