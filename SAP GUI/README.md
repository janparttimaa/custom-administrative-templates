# SAP GUI

This repository includes custom Administrative Templates for SAP GUI that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| SAPGUI | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/SAPGUI/Policy/SAPGUIAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```Language``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/SAPGUI~Policy~SAPGUI/Language``` | String | ```<enabled/> <data id="Language" value="EN"/>```

### Descriptions
More details of the settings can be found this chapter.

#### Language
Set and enforce language of the SAP GUI.

If you want to set language, enable this policy and set prefferred language. If user changes preferred language to something else from SAP GUI's settings, language will be enforced back to preferred language next time when device's policy refresh cycle starts. 

Please check language values in this table below:
<br>_(List updated 17 May 2026)_

| Language | Value | More information |
|---------|---------|---------|
| English | ```EN``` | This is recommended language. |
| Arabic | ```AR``` | |
| Bulgarian | ```BG``` | |
| Catalan | ```CA``` | |
| Chinese | ```ZH``` | |
| Chinese trad. | ```ZF``` | |
| Croatian | ```HR``` | |
| Czech | ```CS``` | |
| Danish | ```DA``` | |
| Dutch | ```NL``` | |
| Estonian | ```ET``` | |
| Finnish | ```FI``` | |
| French | ```FR``` | |
| German | ```DE``` | |
| Greek | ```EL``` | |
| Hebrew | ```HE``` | |
| Hungarian | ```HU``` | |
| Italian | ```IT``` | |
| Japanese | ```JA``` | |
| Korean | ```KO``` | |
| Latvian | ```LV``` | |
| Lithuanian | ```LT``` | |
| Norwegian | ```NO``` | |
| Polish | ```PL``` | |
| Portuguese | ```PT``` | |
| Romanian | ```RO``` | |
| Russian | ```RU``` | |
| Serbian (Latin) | ```SH``` | |
| Slovak | ```SK``` | |
| Slovenian | ```SL``` | |
| Spanish | ```ES``` | |
| Swedish | ```SV``` | |
| Thai | ```TH``` | |
| Turkish | ```TR``` | |
| Ukrainian | ```UK``` | |

If you disable or not configure this setting, user can choose preferred language from SAP GUI's settings and we will not enforce user to use specific language.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Set language
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\SAP\General
- **Value Type:** REG_SZ
- **Value Name:** Language
- **Enabled Value:** ```EN```
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.