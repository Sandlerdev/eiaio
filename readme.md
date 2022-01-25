# Enterprise Integration Application Infrastructure Orchestration (EIAIO)

This repository is intended to host the ARM templates used to deploy application infrastructure associated with various PCB application deployments.

## Repository Structure

Each ARM Template is separated into its own folder with its own readme.md file explaining the infrastructure that will be deployed.

Readme.md files should ideally include a "Deploy to Azure" button as shown here.

![Deploy to Azure](https://aka.ms/deploytoazurebutton)

Clicking this button (in an ARM Template folder) should initiate a "Custom Deployment" in the user's Azure Subscription.

Each (Template) folder should be structured as follows:
```bash
.
|- Folder Name
|    |- ARMTemplates
|    |    |- azureDeploy.json
|    |    |- azureDeploy.parameters.json
|    |    |- NestedTemplates (optional)
|    |    |    |- NestedTemplate.json
|    |    |    |- NestedTemplate2.json
|    |    |    |- readme.md
|    |- readme.md
```

**NestedTemplates\readme.md** files are intended to highlight parameters required for that nested feature so that NestedTemplate features can more easily be used in a variety of combinations.

## Templates

| Name | Description | Azure Services | References |
| ---- | ----------- | -------------- | ---------- |
|CoreDataIngestion| Basic services to ingest IoT Data.  Does not do much on its own, but can be foundation of other solutions.| IoT Hub, Azure Storage|TBD|
|TimeSeries| TimeSeries Data Storage of ingested data.|IoT Hub, Azure Storage, TimeSeries Insights|TBD|
|... |... |... |... |




**[todo]**

The root of this repo contains a generic PowerShell script which can be used to execute each of the ARM templates with their respective parameter files.

