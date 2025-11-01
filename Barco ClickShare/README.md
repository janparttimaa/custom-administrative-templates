# Barco ClickShare

This repository includes custom Administrative Templates for Barco ClickShare that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Barco ClickShare | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/ClickShare/Policy/ClickShareAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```AutoUpdateEnable``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/AutoUpdateEnable``` | String | ```<enabled/> <data id="AutoUpdateEnable" value="examplecompany1&#xF000;examplecompany2&#xF000;examplecompany3&#xF000;examplecompany4"/>```

### Descriptions
More details of the settings can be found this chapter.

#### AutoUpdateEnable
If you want to enforce sign-in you need to enable this setting and define allowed organizations.

More information:


> [!NOTE]  
> - If you set multiple organization domains to the setting value, you need to separate domains using ```&#xF000;``` string. See example from the "Recommended value" above.
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```


##### Technical information
- **Friendly name of the setting:** Enable automatic updates
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\WOW6432Node\Barco\ClickShare Installer
- **Value Type:** REG_MULTI_SZ
- **Value Name:** AutoUpdateEnable
- **Enabled Value:** 

        examplecompany1
        examplecompany2
        examplecompany3
        examplecompany4

- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.