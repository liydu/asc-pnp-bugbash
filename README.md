<!-- markdownlint-disable MD033 -->
# Azure Security Center and IoT Plug and Play with Azure RTOS IoT Middleware Bug Bash

## Intro

IoT Plug and Play Summer Refresh and Azure Security Center module have been enabled in Azure RTOS IoT Middleware. 

Goals for this session:
1. Build and run multiple components IoT Plug and Play sample application.
2. Build and test Azure Security Center integration with Azure RTOS.

### Support and feedback

- Use [ASC and PnP integration in Azure RTOS Bug Bash](https://teams.microsoft.com/l/channel/19%3aab71cb8272f74c6eb4093725dcc85358%40thread.tacv2/ASC%2520and%2520PnP%2520integration%2520in%2520Azure%2520RTOS%2520Bug%2520Bash?groupId=471ee79d-e373-4f62-ae58-9e3944580d35&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) Teams channel for discussion, feedback and asking for help.
- If you get bug or feature request, please use this [Bug Template](https://msazure.visualstudio.com/One/_workitems/create/Bug?templateId=ff1b00b4-9812-4f71-ba79-4693a0ca440d&ownerId=56e4acd1-b6b1-4e8c-b9f3-15683ec2cdc6). You can query existing bugs in this [PnP & ASC BugBash Query](https://msazure.visualstudio.com/One/_queries/query-edit/3f280880-1bbd-488e-91a4-083f62a26b82/)

### Sample projects

For this bug bash, you can choose to test sample projects in IAR Workbench, semi's IDE projects for actual dev boards or simulated device on PC as zipped files:

* ST STM32F746G Discovery Kit
* NXP i.MX RT1060 EVK
* Microchip SAM E54 Xplained Pro EVK
* ST STM32L4+ Discovery Kit IoT Node / ST STM32L475 Discovery Kit IoT Node
* Simulated device on Windows / Linux

Download the `.zip` file for the specific board and tool (IAR, semi's IDE or PC) you have and choose to test against:

[**Azure RTOS IoT Middleware bug bash samples**](https://#OneDrive)

> NOTE: The Azure Security Center experience is currently enabled on all boards and simulated devices except for the STM32L4+ / STM32L475 board.

### Get started

#### Prepare Azure resources

**We recommend to use the IoT Hub (*azure-rtos-asc-bugbash*) that has been created that supports the PnP summer fresh and Azure Security Center for IoT. Please get the IoT Hub connection string that is to be used to configure IoT explorer and your device in the meeting.**

If you prefer to create your own IoT Hub, here are the instructions to do so:

- The Azure Security Center for IoT required hub version is only available in the following regions: canary (EastUS2EUAP, CentralUSEUAP) to have Canary enable for the IoT Hub.
- Create S1 IoTHub in any of these regions to get started.

To create the hub using the `az` CLI replace the hubname and run the script below:

```bash
az extension add --name azure-iot
az login
az account set -s [subscription name]
az iot hub create --resource-group BugBash --sku S1 --location eastus2euap --partition-count 4 --name [iot-hub-name]
```
To create the hub from the portal make sure you select the right subscription that has Canary region enabled.

#### Device specific guides

Device specific guides is provided as PDF with in the docs folder of the zip file. You can use the same [Bug Template](https://msazure.visualstudio.com/One/_workitems/create/Bug?templateId=ff1b00b4-9812-4f71-ba79-4693a0ca440d&ownerId=56e4acd1-b6b1-4e8c-b9f3-15683ec2cdc6) to provide the feedback for the documentation.

When you are following the guide, you can skip the most part of the **Prepare Azure Resources > Create an IoT Hub** section and jump to the last step which is getting the IoT Hub devices host name. Then continue to the **Prepare Azure Resources > Register an IoT Hub device** section to proceed the reset of the guide.

### Reference

#### Digital Twin Definition Language

The DTDL v2 Spec can be found at [https://aka.ms/dtdl](https://aka.ms/dtdl) can be used as a reference for the language. Use the [samples](https://github.com/Azure/opendigitaltwins-dtdl/tree/master/DTDL/v2/samples) we've provided to get started.

* [DTDL VS Code extension](https://marketplace.visualstudio.com/items?itemName=vsciot-vscode.vscode-dtdl)
* [DTDL VS 2019 extension](https://github.com/rido-min/pnp-summer-bugbash/releases/tag/1)

#### IoT Plug and Play

* [IoT Plug and Play preview refresh](https://docs.microsoft.com/azure/iot-pnp/overview-iot-plug-and-play-preview-updates)

#### Azure IoT Middleware for Azure RTOS

* [Azure IoT Embedded SDK](https://github.com/Azure/azure-sdk-for-c/tree/master/sdk/docs/iot)
* [Azure IoT Middleware for Azure RTOS (convenience layer)](https://dev.azure.com/ExpressLogic/X-Ware/_git/netx?path=%2FApplications%2FAZURE_IOT%2Fdocs%2FREADME.md&_a=preview)

#### Azure Security Center

*[TBD]*
