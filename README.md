# IoTHub-128-Partitions

Users can create IoT Hubs with a max of 32 partitions through the Azure Portal. It's undocumented, but you can actually increase the number of partitions to a max of 128 partitions using Azure Resource templates. JSON files for the hub provisioning template as well as an example parameters file is included. 

Run the following az command 
```
az deployment group create --resource-group {rg-Name} --template-file iothub_template.json --parameters iothub_parameters.json
```

<B>Note:</B>
- I use the Azure CLI for this but you can use powershell as well
- Ensure you have the latest Azure CLI installed https://docs.microsoft.com/en-us/cli/azure/install-azure-cli
- Ensure that you have installed the latest version of the Azure IoT CLI Extension https://github.com/Azure/azure-iot-cli-extension#installation

![Image of Hub Provisioned with 128 partitions](https://github.com/ms-vincent/IoTHub-128-Partitions/blob/main/hubprovisioned.jpg)

Parameters file: https://github.com/ms-vincent/IoTHub-128-Partitions/blob/main/iotHub-parameters.json

ARM template: https://github.com/ms-vincent/IoTHub-128-Partitions/blob/main/iotHub-parameters.json
