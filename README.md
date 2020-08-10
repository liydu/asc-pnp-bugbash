<!-- markdownlint-disable MD033 -->
# Azure Security Center and IoT Plug and Play with Azure RTOS IoT Middleware Bug Bash

## Intro

IoT Plug and Play Summer Refresh and Azure Security Center module have been enabled in Azure RTOS IoT Middleware. 

Goals for this session:
1. Build and run multiple components IoT Plug and Play sample application.
2. Build and test Azure Security Center integration with Azure RTOS.

### Support and feedback

- Use our Teams meeting for discussion and asking for help.
- If you get bug or feature request, please use this [Bug Template](https://msazure.visualstudio.com/One/_workitems/create/Bug?templateId=ff1b00b4-9812-4f71-ba79-4693a0ca440d&ownerId=56e4acd1-b6b1-4e8c-b9f3-15683ec2cdc6). You can query existing bugs in this [PnP & ASC BugBash Query](https://msazure.visualstudio.com/One/_queries/query-edit/3f280880-1bbd-488e-91a4-083f62a26b82/)

### Getting started, environment and tooling

For this bug bash, we will provide both IAR Workbench and semi's IDE projects as zipped files that can be found in:

[**Azure RTOS IoT Middleware bug bash samples**](https://#OneDrive)

Download the `.zip` file for the specific board and tool (IAR or semi's IDE) you have and choose to test against:

* [ST STM32L4+ Discovery Kit IoT Node](https://www.st.com/en/evaluation-tools/b-l4s5i-iot01a.html) / [ST STM32L475 Discovery Kit IoT Node](https://www.st.com/en/evaluation-tools/b-l475e-iot01a.html)
* [ST STM32F746G Discovery Kit](https://www.st.com/en/evaluation-tools/32f746gdiscovery.html)
* [NXP i.MX RT1060 EVK](https://www.nxp.com/design/development-boards/i-mx-evaluation-and-development-boards/mimxrt1060-evk-i-mx-rt1060-evaluation-kit:MIMXRT1060-EVK)
* [Microchip SAM E54 Xplained Pro EVK](https://www.microchip.com/developmenttools/productdetails/atsame54-xpro)

#### Docs

Board specific guides is provided as PDF with in the docs folder of the zip file. You can use the same [Bug Template](https://#) to provide the feedback.

### Reference

#### Digital Twin Definition Language

The DTDL v2 Spec can be found at [https://aka.ms/dtdl](https://aka.ms/dtdl) can be used as a reference for the language. Use the [samples](https://github.com/Azure/opendigitaltwins-dtdl/tree/master/DTDL/v2/samples) we've provided to get started.

* [DTDL VS Code extension](https://marketplace.visualstudio.com/items?itemName=vsciot-vscode.vscode-dtdl)
* [DTDL VS 2019 extension](https://github.com/rido-min/pnp-summer-bugbash/releases/tag/1)

#### Azure IoT Middleware for Azure RTOS

* [Azure IoT Embedded SDK](https://github.com/Azure/azure-sdk-for-c/tree/master/sdk/docs/iot)
* [Azure IoT Middleware for Azure RTOS (convenience layer)](https://dev.azure.com/ExpressLogic/X-Ware/_git/netx?path=%2FApplications%2FAZURE_IOT%2Fdocs%2FREADME.md&_a=preview)


