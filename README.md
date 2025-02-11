# Acorn for a .Net Core sample app - Github Explorer
======

This is an Acorn for the sample .NET app from the official [Microsoft Tutorial Documentation](https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/scaling-aspnet-apps/scaling-aspnet-apps?view=aspnetcore-7.0&tabs=login-azure-cli) on .NET. This sample app uses a search form to browse GitHub repositories by name.

## Deploy the .Net Core App

You can deploy the sample web app on the Acorn SaaS Platform with following simple steps.

1. Login to the [Acorn SaaS Platform](https://beta.acorn.io/) using the Github Sign-In option with your Github user.
2. Select the "Create Acorn" option.
3. Choose the source for deploying your Acorns
  * Select "From Acorn Image" to deploy the sample Application
  * Provide a name such as `Dot Net Sample Acorn` and keeping Project's default Region, type in the below Acorn image and choose Create 
    ```bash
    ghcr.io/infracloudio/dotnet-core-acorn:v0.0.1
    ```
4. Now the sample App is provisioned on Acorn SaaS Platform and is available for 2hrs. Upgrade to pro account to keep it running longer.
5. Once the Acorn is running, you can access it by clicking the Endpoint or the redirect link.

## Acorn .Net Core App Details

The Acorn Dashboard is integrated with multiple features such as Events, Logs, Details and accessing the Shell of the Application. Details include the CPU, Memory, Network, Latency, Requests and Errors for the Application.

Explore various available options by clicking the Menu option on your Acorn App.

For more details on using the Acorn Dashboard, check this link - [https://beta-docs.acorn.io/getting-started#exploring-the-acorn-dashboard](https://beta-docs.acorn.io/getting-started#exploring-the-acorn-dashboard)

## What next?
After deploying you can edit the Acorn Application or remove it if no longer needed.

1. Click the Edit option to edit your Acorn's Image. Toggle the Advanced Options switch for additional edit options.
2. Remove the Acorn by selecting the Remove option from your Acorn dashboard.
