# Verification Commands — Azure Static Website Storage

## Project Values

Resource Group:

rg-rce-02-static-website

Storage Account:

sttitoiunit02213434

Azure Region:

northeurope

Project Folder:

02-static-website-storage

## Verify Azure CLI Login

Command:

az account show --output table

Expected result:

The active Azure subscription is shown.

## Verify Resource Group

Command:

az group show --name "rg-rce-02-static-website" --output table

Expected result:

The Resource Group exists before cleanup.

## Verify Storage Account

Command:

az storage account show --name "sttitoiunit02213434" --resource-group "rg-rce-02-static-website" --output table

Expected result:

The Storage Account exists before cleanup and shows ProvisioningState as Succeeded.

## Get Static Website Endpoint

Command:

az storage account show --name "sttitoiunit02213434" --resource-group "rg-rce-02-static-website" --query "primaryEndpoints.web" --output tsv

Expected result:

https://sttitoiunit02213434.z16.web.core.windows.net/

## List Files in the $web Container

Command:

az storage blob list --account-name "sttitoiunit02213434" --container-name '$web' --auth-mode login --output table

Expected result:

index.html and 404.html are listed.

## Cleanup Command

Command:

az group delete --name "rg-rce-02-static-website" --yes

Expected result:

The Resource Group and all project resources are deleted.

## Verify Cleanup

Command:

az group exists --name "rg-rce-02-static-website"

Expected result:

false

## Important Note

Some verification commands were run before cleanup.

After cleanup, commands that check the Storage Account, Static Website endpoint, or $web container will no longer work because those resources have already been deleted.

This is expected and confirms that cleanup was completed.
