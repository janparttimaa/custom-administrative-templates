# VLC

This repository includes custom Administrative Templates for VLC that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-templates
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| VLC | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/VLC/Policy/VLCAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```Lang``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/VLC~Policy~VLC/Lang``` | String | ```<enabled/> <data id="Lang" value="en"/>```

### Descriptions
More details of the settings can be found this chapter.

#### Lang
Set and enforce language of the VLC.

If you want to set language, enable this policy and set prefferred language. If user changes preferred language to something else from VLC's settings, language will be enforced back to preferred language next time when device's policy refresh cycle starts. 

Please check language values in this table below:
<br>_(List updated 22 March 2025)_

| Language | Value | More information
|---------|---------|---------|
| American English | ```en``` | This is recommended language. |
| Arabic | ```ar``` |  |
| Aragonese | ```an``` |  |
| Assamese, Indian | ```as_IN``` |  |
| Asturian | ```ast``` |  |
| Basque | ```eu``` |  |
| Belarusian | ```be``` |  |
| Bengali, Bangla | ```bn``` |  |
| Bodo | ```brx``` |  |
| British English | ```en_GB``` |  |
| Bulgarian | ```bg``` |  |
| Cambodian | ```km``` |  |
| Catalan | ```ca``` |  |
| Chinese Simplified | ```zh_CN``` |  |
| Chinese Traditional | ```zh_TW``` |  |
| Corsican | ```co``` |  |
| Croatian | ```hr``` |  |
| Czech | ```cs``` |  |
| Danish | ```da``` |  |
| Dutch | ```nl``` |  |
| Estonian | ```et``` |  |
| Finnish | ```fi``` |  |
| French | ```fr``` |  |
| Gaelic (Scots Gaelic) | ```gd``` |  |
| Galician | ```gl``` |  |
| German | ```de``` |  |
| Greek | ```el``` |  |
| Gujarati, Indian | ```gu``` |  |
| Hebrew | ```he``` |  |
| Hungarian | ```hu``` |  |
| Icelandic | ```is``` |  |
| Indonesian | ```id``` |  |
| Irish | ```ga``` |  |
| Italian | ```it``` |  |
| Japanese | ```ja``` |  |
| Kannada | ```kn``` |  |
| Kazakh | ```kk``` |  |
| Korean | ```ko``` |  |
| Latvian | ```lv``` |  |
| Lithuanian | ```lt``` |  |
| Malay | ```ms``` |  |
| Marathi | ```mr``` |  |
| Nepali | ```ne``` |  |
| Norwegian Bokmal | ```nb``` |  |
| Norwegian Nynorsk | ```nn``` |  |
| Occitan | ```oc``` |  |
| Polish | ```pl``` |  |
| Portugese Brazilian | ```pt_BR``` |  |
| Portugese Portugal | ```pt_PT``` |  |
| Punhabi, Indian | ```pa``` |  |
| Romanian | ```ro``` |  |
| Russian | ```ru``` |  |
| Serbian - Cyrillic | ```sr``` |  |
| Sinhala | ```si``` |  |
| Slovak | ```sk``` |  |
| Slovenian | ```sl``` |  |
| Spanish | ```es``` |  |
| Spanish Mexico | ```es_MX``` |  |
| Swedish | ```sv``` |  |
| Thai | ```th``` |  |
| Turkish | ```tr``` |  |
| Ukranian | ```uk``` |  |
| Vietnamese | ```vi``` |  |
| Walloon | ```wa``` |  |
| Welsh | ```cy``` |  |

If you disable or not configure this setting, user can choose preferred language from VLC's settings and we will not enforce user to use specific language.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Set language
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\VideoLAN\VLC
- **Value Type:** REG_SZ
- **Value Name:** Lang
- **Enabled Value:** ```en```
- **Disabled Value:** ```en```