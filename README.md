# Custom Administrative Templates (ADMX & ADML)

This repository includes some custom Administrative Templates that can be used on your on-prem environment or Microsoft Intune.

> [!CAUTION]
> [Ingesting](https://petervanderwoude.nl/post/deep-dive-ingesting-third-party-admx-files/) (or [importing](https://learn.microsoft.com/en-us/mem/intune-service/configuration/administrative-templates-import-custom)) custom templates of [Microsoft Windows](https://github.com/janparttimaa/custom-administrative-templates/tree/main/Microsoft%20Windows) are currently not working on Microsoft Intune due to the fact that [Microsoft is currently blocking](https://learn.microsoft.com/en-us/windows/client-management/win32-and-centennial-app-policy-configuration#a-href-idoverviewaoverview) registry entries where custom policies are applying registry keys. Otherwise, the GPOs are working normally as they should be.

## OMA-URI of ADMX-templates
Here you can see OMA-URI information for released ADMX-templates, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Adobe Digital Editions     | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/AdobeDigitalEditions/Policy/AdobeDigitalEditionsAdmx``` |
| 7-Zip     | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/7-Zip/Policy/7-ZipAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of these ADMX-templates, that can be deployed via Intune using ingestion with ingested ADMX-templates.

### Adobe Digital Editions
| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```DoNotInstallAntivirus``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeDigitalEditions~Policy~AdobeDigitalEditions/DoNotInstallAntivirus``` | String | ```<enabled/>```

#### Description (DoNotInstallAntivirus)
During installation of Adobe Digital Edition, the installer might ask you to install antivirus product (e.g. Norton, Symantec etc.) or trial one of those products.

**Recommended:** If you enable this setting, Adobe Digital Edition will not pop up and ask you to install antivirus product into endpoint device running 64-bit Microsoft Windows operating system. This request will be automatically declined. Enabling this policy is required and necessary when deploying Adobe Digital Edition to be available either via Intune Company Portal or Software Center to all users or selected users.

If you disable this setting, Adobe Digital Edition will pop up and ask you to install antivirus product. You can manually either accept or decline the request.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

If you not configure this setting, Adobe Digital Edition might pop up and ask you to install antivirus product depending what setting you have previously set. You can manually either accept or decline the request, if you get the request.
