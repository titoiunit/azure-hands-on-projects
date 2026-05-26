# Cleanup Proof - Project 01

## Deleted Resource Group

```text
rg-azure-hands-on-01
```

## Cleanup Command

```zsh
az group delete --name rg-azure-hands-on-01 --yes --no-wait
```

## Verification Command

```zsh
az group exists --name rg-azure-hands-on-01
```

## Result

```text
false
```

## Cleanup Status

Azure resources for this lab were deleted successfully.
