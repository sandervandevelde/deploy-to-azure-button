# deploy-to-azure-button

This repo show the experience of deploying an ARM template via a click of a button.

## ARM templates are deployed, not BICEP

Although BICEP is now the preferred way of creating Azure deployments as code (Infrastructure as Code or IaC), the ARM templates built from BICEP are actually deployed. 

### Can Github help?

You could let Github actions [create the ARM template](https://stackoverflow.com/questions/66645149/how-to-create-a-deploy-to-azure-button-that-uses-a-bicep-instead-of-an-json-te) each time the BICEP template is checked in...

## Prerequisites

For building (and deploying from prompt):
- AZ CLI (In this demonstration I use the Powershell [AZ module](https://docs.microsoft.com/en-us/powershell/azure/new-azureps-module-az?view=azps-6.4.0))
- AZ Bicep extension

For programming:
- Visual Studio Code
- Visual Studio Code Bicep extension

## installing bicep in AZ

```
az install bicep
az bicep version
az bicep --help
```

## building the ARM template

```
az bicep build --file main.bicep --outdir .
```

## Demonstration of deployment by Button

Hit this button to deploy the ARM template as seen in this repository:

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsandervandevelde%2Fdeploy-to-azure-button%2Fmain%2Fmain.json)

Notice we make use of this link: 'https://portal.azure.com/#create/Microsoft.Template/uri/[url of arm template]' which we feed with the raw https://raw.githubusercontent.com/sandervandevelde/deploy-to-azure-button/main/main.json. The raw url is [URL encoded](https://www.urlencoder.org/).  

### Example of portal experience

#### Deployment

![image](https://user-images.githubusercontent.com/694737/134773163-95e6bd1f-d991-4d20-a94a-032b3a507c1a.png)

_Note_: The selection of the resourcegroup is not part of the BICEP / ARM template. It expects a resource is available. This selection is provided by the portal.

_Note_: The input parameter is defined in the BICEP / ARM template.

#### Succesful deployment

![image](https://user-images.githubusercontent.com/694737/134773909-84c8452a-6173-4269-94a0-69d1fa3fdf55.png)

#### Output parameters

![image](https://user-images.githubusercontent.com/694737/134773431-ea664341-6846-456b-b63b-9f322fb16bc5.png)

_Note_: output values being a secret are shown without obfuscation!

## Links

Learn about BICEP quickstart:

https://docs.microsoft.com/en-us/azure/azure-resource-manager/bicep/quickstart-create-bicep-use-visual-studio-code?tabs=CLI

Creating an 'Deploy to Azure function':
https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-to-azure-button

