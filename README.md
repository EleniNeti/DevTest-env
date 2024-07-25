The bicep script creates a new DevTestLabs instance that includes a claimed Ubuntu 22.04 LTS server Virtual Machine.
Family/size was chosen Standard_B1ls for billing purposes and to support baseline workflow.

The template deploys the corresponding Azure Infra and PaaS components:

Virtual Network, the DevTest Lab related to a Storage Account for file uploading, a key vault as a security measure to hold users' keys as well as the Virtual Machine itself with its disk attached.

in the Command line:

```bash 
az login 
az group create --name <resource-group-name> --location <location>
az deployment group create --resource-group <resource-group-name> --template-file <path-to-template> --parameters <path-to-parameters>
```
