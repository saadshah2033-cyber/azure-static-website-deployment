# Azure Static Website Deployment

A hands-on cloud engineering project demonstrating how to deploy a React application using **Microsoft Azure Blob Storage Static Website Hosting**.

The application was built using React and Vite, compiled into production files, and hosted through an Azure Storage Account's `$web` container.

> **Project status:** Completed. The temporary Azure resources were deleted after deployment, testing, and evidence collection to avoid ongoing costs.

## Project Overview

The goal of this project was to understand the process of hosting a frontend application using Azure Storage, including storage account configuration, static website hosting, blob uploads, public endpoints, and cost management.

## Architecture

```text
React Application
       |
       v
   Vite Build
       |
       v
  Production Files
      (dist/)
       |
       v
 Azure Storage Account
       |
       v
    $web Container
       |
       v
 Azure Static Website
       |
       v
   Public HTTPS Endpoint
```

## Technologies Used

- React
- Vite
- Microsoft Azure
- Azure Storage Account
- Azure Blob Storage
- Static Website Hosting
- Git and GitHub

## Azure Configuration

| Setting | Configuration |
|---|---|
| Storage Account Type | StorageV2 |
| Performance | Standard |
| Redundancy | Locally Redundant Storage (LRS) |
| Access Tier | Hot |
| Static Website Hosting | Enabled |
| Index Document | `index.html` |
| Error Document | `404.html` |
| Public Network Access | Enabled |
| Private Endpoint | Not configured |

## Implementation Steps

1. Created an Azure Storage Account.
2. Configured Standard performance and LRS redundancy.
3. Selected the Hot access tier.
4. Enabled Static Website Hosting.
5. Configured `index.html` as the index document.
6. Configured `404.html` as the error document.
7. Generated the production build using `npm run build`.
8. Uploaded the production files from the `dist` directory into the `$web` container.
9. Uploaded the assets directory while preserving its folder structure.
10. Uploaded the resume PDF included in the production build.
11. Accessed the application through Azure's Primary Endpoint.
12. Tested the website and inspected browser network requests.
13. Reviewed Azure Cost Management and deleted the temporary Resource Group.

## Screenshots

### 1. Storage Account Configuration

![Storage Account Overview](docs/azure-deployment/01-storage-account-overview.png)

### 2. Static Website Configuration

![Static Website Configuration](docs/azure-deployment/02-static-website-configuration.png)

### 3. Primary Endpoint

![Static Website Endpoint](docs/azure-deployment/03-static-website-endpoint.png)

### 4. Blob Container

![Web Container](docs/azure-deployment/04-web-container.png)

### 5. Uploaded Production Files

![Uploaded Website Files](docs/azure-deployment/07-uploaded-website-files.png)

### 6. Deployed Application

![Azure Website](docs/azure-deployment/09-live-azure-website.png)

### 7. Browser Network Inspection

![Network Requests](docs/azure-deployment/12-network-requests.png)

## Key Learnings

Through this project, I gained practical experience with:

- Azure Storage Account creation and configuration.
- Azure Blob Storage and the `$web` container.
- Static website hosting and public HTTPS endpoints.
- Deploying a Vite production build.
- Managing frontend assets and file paths.
- Configuring an error document for React Router fallback.
- Inspecting HTTP requests using browser developer tools.
- Understanding Azure resource management and cost monitoring.

## Cost Management

The project was deployed temporarily using an Azure Free Account.

Cost Management showed no reported costs during the review. After collecting deployment evidence and completing testing, the Resource Group was deleted to prevent ongoing resource usage.

The Azure deployment is no longer active.

## Conclusion

This project provided practical exposure to deploying a frontend application using Microsoft Azure and understanding the fundamental concepts behind cloud storage, static hosting, endpoints, and resource cost management.

**Project Type:** Cloud Engineering / Azure Fundamentals  
**Focus:** Azure Storage and Static Website Hosting
