# Lessons Learned — Azure Static Website Storage

## What I Learned

In this project, I learned how to host a simple static website using Azure Storage Account Static Website hosting.

I learned how Azure can serve static HTML files without using a traditional virtual machine or web server.

## Key Concepts

## Resource Group

A Resource Group is a logical container for Azure resources.

I used one Resource Group for the whole project so cleanup would be simple and safe.

## Storage Account

A Storage Account is the main Azure resource used for storing data.

In this project, it hosted the static website files.

## Blob Storage

Blob Storage stores unstructured data such as HTML files, images, CSS, JavaScript, documents, and other file types.

## Static Website Hosting

Static Website hosting allows Azure Storage to serve static files through a public web endpoint.

## $web Container

When Static Website hosting is enabled, Azure creates a special container called $web.

The website files need to be uploaded into this container.

## index.html

The index.html file is the default page shown when the user opens the website endpoint.

## 404.html

The 404.html file is the error page shown when a user tries to open a page that does not exist.

## Static Website Endpoint

The static website endpoint is the public URL that users can open in a browser.

## AWS Comparison

This project helped me understand the Azure equivalent of AWS S3 static website hosting.

In AWS, static website files are stored in an S3 bucket.

In Azure, static website files are stored in the $web container inside a Storage Account.

## Verification

I verified the project with:

- Azure Portal
- Azure CLI
- Browser testing
- Storage Account checks
- Blob listing commands

## Cleanup

After testing, I deleted the full Resource Group to avoid unnecessary Azure costs.

The cleanup was verified with:

az group exists --name "rg-rce-02-static-website"

The result was:

false

This means the Resource Group no longer exists.

## Cost Safety

I used a small test website, Standard LRS storage, and deleted the Resource Group after testing.

This helped me practice cloud cost safety and avoid leaving unnecessary resources running.

## Interview Summary

I can explain this project as a simple Azure static website project where I created a Resource Group, created a Storage Account, enabled Static Website hosting, uploaded HTML files into the $web container, tested the public endpoint, verified everything with Azure CLI, and deleted the resources afterwards.
