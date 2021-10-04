# Migration from Azure Storage to Netherite for TypeScript

## Starting point

We have a Durable Function using Azure Storage as storage provider. We will transfer this simple Durable Function to [Netherite](https://microsoft.github.io/durabletask-netherite/#/) in three steps:

1. Make it run locally using Azurite as Storage Emulator
2. Make it run hybrid with Blob Storage and EventHub running on Azure while the Function is running locally
3. Deploy it to Azure and make it run in the cloud

We will use the samples provided in the Netherite [sample repository](https://github.com/microsoft/durabletask-netherite/tree/main/samples).

We assume that the storage provider [Azurite](https://docs.microsoft.com/de-de/azure/storage/common/storage-use-azurite?tabs=visual-studio-code) is installed to emulate the storage locally.

Each step is displayed in a different branch. The `main` branch contains the basic setup for our Durable Function relying on the Azure Storage.