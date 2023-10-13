# Github Explorer
======

The web app uses a search form to browse GitHub repositories by name. This sample .NET7 app is part of the official Microsoft Tutorial Documentation on .NET 

Check this link for more details : https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/scaling-aspnet-apps/scaling-aspnet-apps?view=aspnetcore-7.0&tabs=login-azure-cli

## Deploy the Flask App 

You can deploy the sample web app on the Acorn SaaS Platform to test the Application.

### Steps

1. Login into the Acorn SaaS Platform using the Github Sign-In option with your Github user.
2. You can select the "Create Acorn" option to create new Acorns and deploy your Application.
3. Choose the source for deploying your Acorns
  * Select "From Acorn Image" to deploy the sample Application and select its Image
  * Provide any random name such as `web-app` and keeping Project's default Region, type in the below Acorn image and choose Create 
    ```bash
    ghcr.io/infracloudio/dotnet-core-acorn:v0.0.1
    ```
4. Now the sample App is provisioned on Acorn SaaS Platform and is available for upto 2hrs.
5. Once the Acorn is running, you can access it by clicking the Endpoint or the redirect link.

## Acorn Flask App Details

The Acorn Dashboard is integrated with multiple features such as Events, Logs, Details and accessing the Shell of the Application. Details include the CPU, Memory, Network, Latency, Requests and Errors for the Application.

Explore various available options by clicking the Menu option on your Acorn App.

For more details on using the Acorn Dashboard, check this link - 

## Edit the Acorn Application

You can edit your Acorn's Image and Advanced Options by selecting the Edit option 

## Remove Acorn Application

To Remove the Acorn, select the Remove option from your Acorn's Menu.

