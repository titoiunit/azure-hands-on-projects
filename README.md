# Azure Hands-On Projects

A cost-aware Azure learning repository that complements my AWS, Terraform, Docker, and CI/CD work. It is organised as a set of small, explainable labs rather than a collection of always-on resources.

**Current portfolio status:** 2 completed and cleaned up · 1 paused with the constraint documented · 5 planned scaffolds

## How to read this repository

- **Completed** means the repository contains the implementation or manual-lab evidence and the cleanup record.
- **Paused** means a real constraint was investigated and documented; it is not presented as a shipped solution.
- **Planned scaffold** means the folder contains the exact build and evidence contract, but no deployment is claimed.

A project becomes a featured portfolio case study only after it has implementation, validation evidence, operational notes, and cleanup instructions.

## Labs

| Lab | Status | Focus | Cloud-engineering signal |
| --- | --- | --- | --- |
| [01 — Resource Group + Private Blob Storage](01-resource-group-and-storage/) | Completed + cleaned up | Azure CLI, private object storage, provider registration | Control-plane troubleshooting, resource boundaries, lifecycle discipline |
| [02 — Static Website on Azure Storage](02-static-website-storage/) | Completed + cleaned up | Storage static website hosting | Low-operations delivery, validation, public-edge trade-off |
| [03 — Linux VM Feasibility Assessment](03-linux-vm-web-server/) | Paused before deployment | VM SKU, quota, region, and cost constraints | Investigate, choose not to overspend, document the decision |
| [04 — Serverless Function API](04-serverless-function-api/) | Planned scaffold | HTTP-triggered Function, logging, validation | Serverless API design and runtime operations |
| [05 — Event-Driven Blob Processing](05-event-driven-blob-processing/) | Planned scaffold | Storage event → Function → processed output | Asynchronous design, idempotency, retry thinking |
| [06 — Container App Deployment](06-container-app-deployment/) | Planned scaffold | Container image, revision, health checks, logs | Application delivery without Kubernetes overhead |
| [07 — Monitoring and Alerts](07-monitoring-and-alerts/) | Planned scaffold | Azure Monitor, actionable alerts, runbooks | Operability, signal quality, incident response |
| [08 — Terraform Azure Foundation](08-terraform-azure-foundation/) | Planned scaffold | Modules, environments, remote state, CI | Repeatable IaC and federated identity |

### Suggested review path

1. Start with [Lab 01](01-resource-group-and-storage/) for Azure CLI, private storage, troubleshooting, and cleanup evidence.
2. Continue to [Lab 02](02-static-website-storage/) for a completed delivery case study with verification records.
3. Read [Lab 03](03-linux-vm-web-server/) for a documented cost-and-capacity decision.
4. Use Labs [04](04-serverless-function-api/)–[08](08-terraform-azure-foundation/) as the implementation roadmap; they are blueprints, not completed deployments.

## Repository structure

```text
01-resource-group-and-storage/   completed private-storage lab + cleanup proof
02-static-website-storage/       completed static-site lab + source + verification
03-linux-vm-web-server/          paused feasibility assessment + investigation notes
04-serverless-function-api/      planned implementation blueprint
05-event-driven-blob-processing/ planned implementation blueprint
06-container-app-deployment/     planned implementation blueprint
07-monitoring-and-alerts/        planned implementation blueprint
08-terraform-azure-foundation/   planned implementation blueprint
```

## Definition of done

A lab is not “done” because the resources exist. It needs:

1. Terraform/Bicep or reproducible deployment instructions.
2. A concise architecture diagram and reason for the chosen services.
3. A validation checklist or captured evidence.
4. Security, reliability, and cost trade-offs.
5. Explicit cleanup steps and, where practical, cleanup proof.
6. A 30-second interview explanation.

## Cost guardrails

- Prefer Azure free-tier-eligible and short-lived resources.
- Tag resources with an owner and cleanup date.
- Do not leave VMs, public IPs, managed databases, registry images, or monitoring retention running without a reason.
- Destroy resources immediately after validation and record what was removed.
- Treat subscription, regional SKU, and quota constraints as design inputs — not as reasons to overspend.

## Related portfolio

The cross-cloud overview, AWS case studies, interview stories, lab standard, and cost-aware roadmap are maintained in [cloud-engineering-portfolio](https://github.com/titoiunit/cloud-engineering-portfolio).
