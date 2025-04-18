# Adobe Digital Editions

This repository includes custom Administrative Templates for Adobe Digital Editions that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Adobe Digital Editions | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/AdobeDigitalEditions/Policy/AdobeDigitalEditionsAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```DoNotInstallAntivirus``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeDigitalEditions~Policy~AdobeDigitalEditions/DoNotInstallAntivirus``` | String | ```<enabled/>```

### Descriptions
More details of the settings can be found this chapter.

#### DoNotInstallAntivirus
During installation of Adobe Digital Edition, the installer might ask you to install antivirus product (e.g. Norton, Symantec etc.) or trial one of those products.

**Recommended:** If you enable this setting, Adobe Digital Edition will not pop up and ask you to install antivirus product into endpoint device running 64-bit Microsoft Windows operating system. This request will be automatically declined. Enabling this policy is required and necessary when deploying Adobe Digital Edition to be available either via Intune Company Portal or Software Center to all users or selected users.

If you disable this setting, Adobe Digital Edition will pop up and ask you to install antivirus product. You can manually either accept or decline the request.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

If you not configure this setting, Adobe Digital Edition might pop up and ask you to install antivirus product depending what setting you have previously set. You can manually either accept or decline the request, if you get the request.

##### Technical information
- **Friendly name of the setting:** Do not offer Antivirus program installation
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Wow6432Node\Symantec\NPInstaller\DeclineCount\adobeebook
- **Value Type:** REG_DWORD
- **Value Name:** ns
- **Enabled Value:** 3
- **Disabled Value:** 0
