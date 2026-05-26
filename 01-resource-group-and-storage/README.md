# 01 - Resource Group and Storage Foundation

## Goal

Create the first Azure foundation using a free-tier-first approach.

## What I Built

- Azure Resource Group
- Azure Storage Account
- Private Azure Blob Container
- Test file upload to Blob Storage
- Azure CLI verification workflow
- Screenshot documentation
- Cleanup proof

## Azure Region

```text
northeurope
```

## Resource Names

```text
Resource Group: rg-azure-hands-on-01
Storage Account: sttitam1779789277
Container: lab-container
```

## Architecture

```text
Local macOS Terminal
→ Azure CLI
→ Azure Subscription
→ Resource Group
→ Storage Account
→ Blob Container
→ Uploaded test file
```

## Commands Practiced

```zsh
az login
az account show
az provider register --namespace Microsoft.Storage
az group create
az group show
az storage account create
az storage account show
az storage container create
az storage container list
az storage blob upload
az storage blob list
```

## Troubleshooting

During this project, Azure Storage Account creation initially failed with:

```text
SubscriptionNotFound
```

The issue was fixed by registering the Microsoft.Storage resource provider:

```zsh
az provider register --namespace Microsoft.Storage
```

This helped me understand that Azure services depend on resource providers, and some providers may need to be registered before creating resources.

## Cost Safety

This lab uses a small Azure Storage setup for learning.

Free-tier-first rules:

- Use simple learning resources
- Use Standard_LRS for basic storage redundancy
- Do not commit keys or secrets
- Delete resources after the lab
- Keep cleanup proof in the repo

## Screenshots

```text
screenshots/01-resource-group.png
screenshots/02-storage-account.png
screenshots/03-blob-container.png
screenshots/04-uploaded-blob.png
```

## What I Learned

In this project, I learned how to create a basic Azure foundation using Azure CLI.

I practiced creating a resource group, deploying a storage account, creating a private blob container, uploading a test file, and verifying the result from the command line.

I also learned how to troubleshoot Azure resource provider issues and document the fix clearly.

This project helped me understand how Azure resources are grouped, named, tagged, tested, documented, and cleaned up safely.

## Cleanup Proof

Cleanup command:

```zsh
az group delete --name rg-azure-hands-on-01 --yes --no-wait
```

Cleanup verification:

```zsh
az group exists --name rg-azure-hands-on-01
```

Expected result after cleanup:

```text
false
```
