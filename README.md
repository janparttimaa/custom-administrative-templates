# Custom Administrative Templates (ADMX & ADML)

This repository includes some custom Administrative Templates that can be used on your on-prem environment or Microsoft Intune.

> [!CAUTION]
> [Ingesting](https://petervanderwoude.nl/post/deep-dive-ingesting-third-party-admx-files/) (or [importing](https://learn.microsoft.com/en-us/mem/intune-service/configuration/administrative-templates-import-custom)) custom templates of [Microsoft Windows](https://github.com/janparttimaa/custom-administrative-templates/tree/main/Microsoft%20Windows) are currently not working on Microsoft Intune due to the fact that [Microsoft is currently blocking](https://learn.microsoft.com/en-us/windows/client-management/win32-and-centennial-app-policy-configuration#a-href-idoverviewaoverview) registry entries where custom policies are applying registry keys.

## OMA-URI of ADMX-templates
Here you can see OMA-URI information for released ADMX-templates, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Adobe Digital Editions     | ./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/AdobeDigitalEditions/Policy/AdobeDigitalEditionsAdmx |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of these ADMX-templates, that can be deployed via Intune using ingestion with ingested ADMX-templates.

### Adobe Digital Editions
| Name | Description | OMA-URI | Data type | Value 
|---------|---------|---------|---------|---------|
| DoNotInstallAntivirus | During installation of Adobe Digital Edition, the installer might ask you to install antivirus product (e.g. Norton, Symantec etc.) or trial one of those products.<br>If you enable this setting, those will not be installed. | ./Device/Vendor/MSFT/Policy/AdobeDigitalEditions~Policy~AdobeDigitalEditions/DoNotInstallAntivirus | String | <enabled/>
