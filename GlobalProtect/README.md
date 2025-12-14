# GlobalProtect

This repository includes custom Administrative Templates for GlobalProtect that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| GlobalProtect | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/GlobalProtect/Policy/GlobalProtectAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```Portal``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GlobalProtect~Policy~GlobalProtect/Portal``` | String | ```<enabled/> <data id="Portal" value="vpn.example.com"/>```
| ```Prelogon``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GlobalProtect~Policy~GlobalProtect/Prelogon``` | String | ```<enabled/> <data id="Prelogon" value="1"/>```

### Descriptions
More details of the settings can be found this chapter.

#### Portal
This setting specifies the default portal IP address (or hostname).

Example:
```vpn.example.com```

If you disable or not configure this setting, user can define default portal IP address (or hostname) and we are not enforcing it.

More information [here](https://docs.paloaltonetworks.com/globalprotect/administration/globalprotect-apps/deploy-app-settings-transparently/deploy-app-settings-to-windows-endpoints/deploy-app-settings-in-the-windows-regsitry).

> [!NOTE]
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Portal Address
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Palo Alto Networks\GlobalProtect\PanSetup
- **Value Type:** REG_SZ
- **Value Name:** Portal
- **Enabled Value:** vpn.example.com
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Prelogon
This setting enables GlobalProtect to initiate a VPN tunnel before a user logs in to the device and connects to the GlobalProtect portal.

To enable prelogon from GlobalProtect-client, enable this setting and set following value number: ```1```

If you want to disable prelogon, please disable this setting. 

Please note, that setting this as "Not Configured" will not disable prelogon.

More information [here](https://docs.paloaltonetworks.com/globalprotect/administration/globalprotect-apps/deploy-app-settings-transparently/customizable-globalprotect-app-settings#id51e0e000-9cce-425d-a4fd-e7fe51e1c8fb).

> [!NOTE]
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Enable Prelogon
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Palo Alto Networks\GlobalProtect\PanSetup
- **Value Type:** REG_SZ
- **Value Name:** Prelogon
- **Enabled Value:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.