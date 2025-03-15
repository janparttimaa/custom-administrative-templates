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

### 7-Zip
| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```SetLanguage``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/7-Zip~Policy~7-Zip/SetLanguage``` | String | ```<enabled/> <data id="Lang" value "-"/>```

#### Description (SetLanguage)
Set and enforce language of the 7-Zip.

If you want to set language, enable this policy and set prefferred language. If user changes preferred language to something else from 7-Zip's settings, language will be enforced back to preferred language next time when device's policy refresh cycle starts. 

Please check language values in this table below:

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
