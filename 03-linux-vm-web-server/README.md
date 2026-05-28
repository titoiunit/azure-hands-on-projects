# Azure Hands-on Portfolio Project 03 — Linux VM Web Server

## Status

Paused before deployment due to Azure subscription, VM SKU, and quota limitations.

## Overview

The goal of this project was to create a small Ubuntu Linux Virtual Machine in Microsoft Azure, connect to it using SSH, install NGINX, and test the web server through a public IP address.

This project was planned as the Azure equivalent of a basic AWS EC2 web server lab.

## What I Tried to Build

The planned architecture was:

- Azure Resource Group
- Ubuntu Linux Virtual Machine
- SSH public key authentication
- Public IP address
- Network Security Group
- SSH access on port 22
- HTTP access on port 80
- NGINX web server

## What Happened

The VM deployment was stopped at the VM size selection step.

The intended VM size was Standard_B1s because it is a small, low-cost, free-services-eligible VM size.

However, Azure showed that Standard_B1s was not available for my current subscription in North Europe.

The Azure Portal showed:

- Standard_B1s
- free services eligible
- NotAvailableForSubscription
- Region: North Europe

I also tested other small VM size families, but the available options were not suitable for this cost-safe learning lab.

## Quota and Subscription Limitation

I checked Azure Quotas and discovered that my current subscription was not eligible for quota adjustment.

Azure showed:

Ineligible for quota adjustment.
Azure subscription 1 is not eligible for quota adjustment.
Consider upgrading your subscription.

I registered the required Azure resource providers:

- Microsoft.Compute
- Microsoft.Network
- Microsoft.Quota

After registration, the providers showed as Registered.

However, the subscription still could not request quota increases.

## Decision

I decided not to deploy a larger or more expensive VM size.

The reason is simple: this is a learning and portfolio lab, and the goal is to keep Azure usage cost-safe.

Instead of forcing the deployment, I paused the project and documented the real-world limitation.

This was the correct cloud engineering decision:

- Do not deploy expensive resources just to complete a lab
- Understand the subscription limitation
- Avoid unnecessary cloud costs
- Document the issue clearly
- Clean up any created resources
- Continue with safer Azure labs that do not require VM quota

## Screenshots

This project includes screenshots showing the attempted setup:

- Resource group review in North Europe
- VM Basics configuration with Ubuntu Server 24.04 LTS
- SSH public key field and inbound port selection
- Standard_B1s NotAvailableForSubscription error
- OS disk configured as Standard SSD
- Final validation failure before deployment

## Cost Safety

No virtual machine was deployed.

If the resource group exists, it should be deleted with:

    az group delete --name rg-rce-03-linux-vm-web-server --yes --no-wait

The resource group can be checked with:

    az group exists --name rg-rce-03-linux-vm-web-server

Expected safe result:

    false

## What I Learned

I learned that Azure VM deployment depends on:

- Subscription type
- Region
- VM SKU availability
- vCPU quota
- Resource provider registration
- Quota adjustment eligibility

I also learned that free-services-eligible does not always mean that the VM size is available for every subscription in every region.

This was a useful real-world cloud lesson. Sometimes the right decision is not to continue deploying, but to stop, investigate, avoid unnecessary costs, and document the limitation professionally.

## AWS Comparison

This project was planned as the Azure equivalent of an AWS EC2 web server lab.

The mapping would have been:

- Azure Virtual Machine = AWS EC2 Instance
- Azure Network Security Group = AWS Security Group
- Azure Public IP = EC2 Public IPv4
- SSH port 22 = SSH access to Linux server
- HTTP port 80 = browser access to web server
- NGINX = web server running on the VM

## Next Step

Continue with Azure hands-on projects that do not require VM quota.

Return to this VM lab later only if:

- the subscription is upgraded,
- small VM sizes become available in North Europe,
- quota adjustment becomes available,
- or another safe Azure subscription is used.

## Interview Summary

I started an Azure Linux VM web server lab where the goal was to deploy an Ubuntu VM, connect with SSH, install NGINX, and test it through a public IP.

The deployment stopped at the VM size selection stage because the small low-cost VM size Standard_B1s was not available for my subscription in North Europe.

I investigated the issue using Azure Portal and Azure CLI, registered the required resource providers, checked quota settings, and confirmed that the subscription was not eligible for quota adjustment.

Because I wanted to keep the lab cost-safe, I decided not to deploy a larger VM. I paused the project, documented the limitation, and made sure no unnecessary resources were left running.

This taught me that cloud work is not only about deploying resources, but also about understanding limits, managing cost risk, and making safe engineering decisions.
