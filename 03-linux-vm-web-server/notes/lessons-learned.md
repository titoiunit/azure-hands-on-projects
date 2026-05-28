# Lessons Learned — Azure Linux VM Web Server

## Project Status

This project was paused before deploying the virtual machine.

The goal was to create a small Ubuntu Linux Virtual Machine in Azure, connect to it using SSH, install NGINX, and test the web server through a public IP address.

However, the deployment was stopped at the VM size selection step because the required low-cost VM size was not available for my current Azure subscription in North Europe.

## What Happened

I wanted to use North Europe as the only region for this lab.

During the VM creation process, I tried to select a small cost-safe VM size such as:

- Standard_B1s
- Other small B-series sizes
- Small A-series fallback sizes
- Small D-series fallback sizes

The Azure Portal showed that `Standard_B1s` was free services eligible, but it was not available for my subscription in North Europe.

The Azure CLI also confirmed that `Standard_B1s` had the restriction:

```text
NotAvailableForSubscription
