# Azure Hands-On Projects

A cost-aware Azure learning repository that complements my AWS, Terraform, Docker, and CI/CD work. The goal is not to claim an always-on production platform; it is to build small, explainable labs with clear validation, operational reasoning, and cleanup.

## Recruiter guide

This repository demonstrates how I transfer core cloud-engineering patterns across providers:

- secure storage and static delivery
- network boundaries and identity
- serverless and event-driven design
- container deployment
- monitoring and alerting
- Infrastructure as Code with Terraform

Each lab becomes a featured portfolio item only when it includes implementation, a validation record, documented trade-offs, and cleanup instructions.

## Learning workstreams

| Path | Focus | Cloud-engineering signal |
| --- | --- | --- |
| `01-resource-group-and-storage` | Resource groups and storage | Resource organisation, tags, access boundaries |
| `02-static-website` | Storage-based static site | CDN/edge delivery and low-ops hosting |
| `03-linux-vm-web-server` | Linux VM workload | Networking, administration and cost controls |
| `04-serverless-function-api` | Function-based API | Event-driven compute and API design |
| `05-event-driven-blob-processing` | Blob-triggered processing | Asynchronous processing and failure handling |
| `06-container-app-deployment` | Container Apps | Image-to-runtime deployment and runtime configuration |
| `07-monitoring-and-alerts` | Azure Monitor | Signals, alerts and incident response |
| `08-terraform-azure-foundation` | Terraform foundation | Repeatable provider-agnostic Infrastructure as Code |

## Definition of done for a lab

A lab is not “done” because the resources exist. It needs:

1. Terraform or reproducible deployment instructions.
2. A concise architecture diagram and the reason for the chosen services.
3. A validation checklist or captured evidence.
4. Security, reliability, and cost trade-offs.
5. Explicit cleanup steps.

## Cost guardrails

- Prefer the Azure free tier and short-lived test resources.
- Tag every resource with an owner and cleanup date.
- Avoid leaving VMs, public IPs, managed databases, and monitoring retention running unnecessarily.
- Destroy resources immediately after validation and record what was removed.

## Related portfolio

The cross-cloud overview, AWS case studies, interview stories, and lab standard are maintained in [cloud-engineering-portfolio](https://github.com/titoiunit/cloud-engineering-portfolio).