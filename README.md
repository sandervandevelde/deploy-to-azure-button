# deploy-to-azure-button

## Prerequisites

For building and deploying:
- AZ CLI in 
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

## Demonstration

Hit this button to deploy the ARM template as seen in this repository:

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsandervandevelde%2Fdeploy-to-azure-button%2Fmain%2Fmain.json)

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
Creating an 'Deploy to Azure function':
https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-to-azure-button

