# kudos-backend-functions
Infrastructure for implementing Kudos API backend on Node.JS in Azure Functions. Functions source code is maintained in [kudos-functions-code](https://github.com/azurecz/kudos-functions-code).

# Deploy complete solution from master template
Go to kudos repo and use master template to provision all components of the solution.

# Deploy API Management via portal
Click button and follow wizard.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fgithub.com%2Fazurecz%2Fkudos-backend-fnctions%2Fraw%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

# Deploy API Management from GitHub
```
az group create -n kudos -l westeurope
az group deployment create -g kudos \
    --template-uri https://github.com/azurecz/kudos-backend-functions/raw/master/azuredeploy.json
```

# Deploy API Management from local
```
az group create -n kudos -l westeurope
az group deployment create -g kudos --template-file azuredeploy.json
```