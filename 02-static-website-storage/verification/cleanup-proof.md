# Cleanup Proof — Azure Static Website Storage

## Cleanup Command

The Azure resources for this project were deleted by deleting the full Resource Group:

```zsh
az group delete \
  --name "rg-rce-02-static-website" \
  --yes
