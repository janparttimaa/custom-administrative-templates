# Microsoft Windows - Custom Settngs

This repository includes custom Administrative Templates for "Microsoft Windows - Custom Settngs" that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| MicrosoftWindowsCustomSettings | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/MicrosoftWindowsCustomSettings/Policy/MicrosoftWindowsCustomSettingsAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```HideFileExt``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/MicrosoftWindowsCustomSettings~Policy~MicrosoftWindowsCustomSettings/HideFileExt``` | String | ```<disabled/>```

### Descriptions
More details of the settings can be found this chapter.

#### HideFileExt
This setting controls whether file name extensions are displayed in File Explorer.

- **Enabled:** File name extensions are hidden in File Explorer.
- **Disabled:** File name extensions are visible in File Explorer.

If a user changes this setting manually, the policy will revert the value to the administrator-specified configuration.

> [!NOTE]
> - Setting this policy to "Not Configured" will not restore the original system behavior. To revert to the original setting, ensure that the policy is explicitly set as "Enabled".
> - When disabling or enabling this setting, policy will apply next time when device will be restarted.

> [!NOTE]
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Hide file name extensions
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced
- **Value Type:** REG_DWORD
- **Value Name:** HideFileExt
- **Enabled Value:** 1
- **Disabled Value:** 0