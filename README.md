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


[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsandervandevelde%2Fdeploy-to-azure-button%2Fmain%2Fmain.bicep)
