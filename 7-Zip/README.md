# 7-Zip

This repository includes custom Administrative Templates for 7-Zip that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-templates
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| 7-Zip | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/7-Zip/Policy/7-ZipAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```Lang``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/7-Zip~Policy~7-Zip/Lang``` | String | ```<enabled/> <data id="Lang" value="-"/>```

### Descriptions
More details of the settings can be found this chapter.

#### Lang
Set and enforce language of the 7-Zip.

If you want to set language, enable this policy and set prefferred language. If user changes preferred language to something else from 7-Zip's settings, language will be enforced back to preferred language next time when device's policy refresh cycle starts. 

Please check language values in this table below:
<br>_(List updated 22 March 2025)_

| Language | Value | More information
|---------|---------|---------|
| English | ```-``` | This is default language. |
| Afrikaans | ```af``` ||
| Albanian | ```sq``` ||
| Arabic | ```ar``` ||
| Aragonese | ```an``` ||
| Armenian | ```hy``` ||
| Asturian | ```ast``` ||
| Azerbaijani | ```az``` ||
| Bangla | ```bn``` ||
| Bashkir | ```ba``` ||
| Basque | ```eu``` ||
| Belarusian | ```be``` ||
| Breton | ```br``` ||
| Bulgarian | ```bg``` ||
| Catalan | ```ca``` ||
| Chinese Simplified | ```zh-cn``` ||
| Chinese Traditional | ```zh-tw``` ||
| Corsican | ```co``` ||
| Croatian | ```hr``` ||
| Czech | ```cs``` ||
| Danish | ```da``` ||
| Dutch | ```nl``` ||
| Esperanto | ```eo``` ||
| Estonian | ```et``` ||
| Extremaduran | ```ext``` ||
| Farsi | ```fa``` ||
| Finnish | ```fi``` ||
| French | ```fr``` ||
| Frisian | ```fy``` ||
| Friulian | ```fur``` ||
| Galician | ```gl``` ||
| Georgian | ```ka``` ||
| German | ```de``` ||
| Greek | ```el``` ||
| Gujarati, Indian | ```gu``` ||
| Hebrew | ```he``` ||
| Hindi, Indian | ```hi``` ||
| Hungarian | ```hu``` ||
| Icelandic | ```is``` ||
| Ido | ```io``` ||
| Indonesian | ```id``` ||
| Irish | ```ga``` ||
| Italian | ```it``` ||
| Japanese | ```ja``` ||
| Kabyle | ```kab``` ||
| Karakalpak - Latin | ```kaa``` ||
| Kazakh | ```kk``` ||
| Korean | ```ko``` ||
| Kurdish | ```ku``` ||
| Kurdish - Sorani | ```ku-ckb``` ||
| Kyrgyz | ```ky``` ||
| Latvian | ```lv``` ||
| Ligurian | ```lij``` ||
| Lithuanian | ```lt``` ||
| Macedonian | ```mk``` ||
| Malay | ```ms``` ||
| Marathi | ```mr``` ||
| Mongolian (MenkCode) | ```mng2``` ||
| Mongolian (Unicode) | ```mng``` ||
| Mongolian | ```mn``` ||
| Nepali | ```ne``` ||
| Norwegian Bokmal | ```nb``` ||
| Norwegian Nynorsk | ```nn``` ||
| Pashto | ```ps``` ||
| Polish | ```pl``` ||
| Portugese Brazilian | ```pt-br``` ||
| Portugese Portugal | ```pt``` ||
| Punhabi, Indian | ```pa-in``` ||
| Romanian | ```ro``` ||
| Russian | ```ru``` ||
| Sanskrit, Indian | ```sa``` ||
| Serbian - Cyrillic | ```sr-spc``` ||
| Serbian - Latin | ```sr-spl``` ||
| Sinhala | ```si``` ||
| Slovak | ```sk``` ||
| Slovenian | ```sl``` ||
| Spanish | ```es``` ||
| Swahili | ```sw``` ||
| Swedish | ```sv``` ||
| Tajik | ```tg``` ||
| Tamil | ```ta``` ||
| Tatar | ```tt``` ||
| Thai | ```th``` ||
| Turkish | ```tr``` ||
| Turkmen | ```tk``` ||
| Ukranian | ```uk``` ||
| Uyghur | ```ug``` ||
| Uzbek | ```uz``` ||
| Uzbek - Cyrillic | ```uz-cyrl``` ||
| Valencian | ```va``` ||
| Vietnamese | ```vi``` ||
| Welsh | ```cy``` ||
| Yoruba | ```yo``` ||

If you disable or not configure this setting, user can choose preferred language from 7-Zip's settings and we will not enforce user to use specific language.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Set language
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\7-Zip
- **Value Type:** REG_SZ
- **Value Name:** Lang
- **Enabled Value:** ```-```
- **Disabled Value:** ```-```