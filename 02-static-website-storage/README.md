# Azure Hands-on Portfolio Project 02 — Static Website Storage

## Overview

This project demonstrates how to host a simple static website using Azure Storage Account Static Website hosting.

The goal was to build a beginner-friendly Azure version of an AWS S3 static website project and document the full process for a cloud engineering portfolio.

## What I Built

I built a simple static website using:

- Azure Resource Group
- Azure Storage Account
- Azure Blob Storage
- Static Website hosting
- `$web` container
- `index.html`
- `404.html`
- Public static website endpoint
- Azure CLI verification
- Safe cleanup after testing

## Azure Services Used

| Service | Purpose |
|---|---|
| Azure Subscription | Billing and resource boundary |
| Resource Group | Logical container for project resources |
| Storage Account | Main storage resource |
| Blob Storage | Stores static website files |
| Static Website Hosting | Serves the website from Azure Storage |
| `$web` Container | Special container for static website content |
| Azure CLI | Used for verification and cleanup |

## Architecture Flow

```text
User Browser
    ↓
Azure Static Website Endpoint
    ↓
Azure Storage Account
    ↓
$web Container
    ↓
index.html / 404.html
