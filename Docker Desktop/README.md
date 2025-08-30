# Docker Desktop

This repository includes custom Administrative Templates for Docker Desktop that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Docker Desktop | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/DockerDesktop/Policy/DockerDesktopAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```AllowedOrgs``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/DockerDesktop~Policy~DockerDesktop/AllowedOrgs``` | String | ```<enabled/> <data id="AllowedOrgs" value="example.com&#xF000;example2.com&#xF000;example3.com&#xF000;example4.com"/>```

### Descriptions
More details of the settings can be found this chapter.

#### AllowedOrgs
If you want to enforce sign-in you need to enable this setting and define allowed organizations.

More information:
https://docs.docker.com/enterprise/security/enforce-sign-in/

> [!NOTE]  
> - If you set multiple organization domains to the setting value, you need to separate domains using ```&#xF000;``` string. See example from the "Recommended value" above.
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```


##### Technical information
- **Friendly name of the setting:** Enforce sign-in
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Docker\Docker Desktop
- **Value Type:** REG_MULTI_SZ
- **Value Name:** AllowedOrgs
- **Enabled Value:** 

        example.com 
        example2.com
        example3.com
        example4.com

- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.