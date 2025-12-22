# WinZip

This repository includes custom Administrative Templates for WinZip that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| WinZip | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/WinZip/Policy/WinZipAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```AutoMode``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/WinZip~Policy~WinZip/AutoMode```<br>```./User/Vendor/MSFT/Policy/Config/WinZip~Policy~WinZip/AutoMode``` | String | ```<enabled/> <data id="AutoMode" value="0"/>```
| ```DisablePersonalContacts``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/WinZip~Policy~WinZip/DisablePersonalContacts``` | String | ```<enabled/> <data id="DisablePersonalContacts" value="1"/>```
| ```InstallBGDD``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/WinZip~Policy~WinZip/InstallBGDD``` | String | ```<enabled/> <data id="InstallBGDD" value="0"/>```
| ```NoUpdateChecking``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/WinZip~Policy~WinZip/NoUpdateChecking```<br>```./User/Vendor/MSFT/Policy/Config/WinZip~Policy~WinZip/NoUpdateChecking``` | String | ```<enabled/> <data id="NoUpdateChecking" value="1"/>```

### Descriptions
More details of the settings can be found this chapter.

#### AutoMode
If you want to suppress updater, enable this policy and set value 0.

If you don't want to suppress updater, enable this policy and set value 1.

More information [here](https://stealthpuppy.com/disabling-check-for-winzip-update/).

> [!NOTE]
> - **Important:** Configure this policy to User and Device contexts.
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<enabled/> <data id="AutoMode" value="0"/>```

##### Technical information
- **Friendly name of the setting:** [Software Updates] Suppress updater
- **Registry Hive:** HKEY_LOCAL_MACHINE / HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Nico Mak Computing\WinZip\UpdateCheck
- **Value Type:** REG_SZ
- **Value Name:** AutoMode
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that the registry key does not exist. In this case, the application uses the default value that is hardcoded in the application, and the setting is therefore not disabled, even though the registry value no longer exists (or application may re-create default registry value again). If you want to disable the setting via Intune, please ensure that value is then set to ```<enabled/> <data id="AutoMode" value="0"/>```

#### DisablePersonalContacts
If you want to completely disable possibility to use personal email address on WinZip Emailer, enable this policy and set value 1.

If you don't want to disable possibility to use personal email address on WinZip Email, enable this policy and set value 0.

More information [here](https://kb.corel.com/Attachments/kcs-189030/WZ27-Enterprise-Installation-and-Configuration-Guide.pdf).

> [!NOTE]
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<enabled/> <data id="DisablePersonalContacts" value="0"/>```

##### Technical information
- **Friendly name of the setting:** [WinZip Emailer] Disable possibility to use personal email address
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Nico Mak Computing\WinZip\Policies
- **Value Type:** REG_SZ
- **Value Name:** DisablePersonalContacts
- **Enabled Value:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that the registry key does not exist. In this case, the application uses the default value that is hardcoded in the application, and the setting is therefore not disabled, even though the registry value no longer exists (or application may re-create default registry value again). If you want to disable the setting via Intune, please ensure that value is then set to ```<enabled/> <data id="DisablePersonalContacts" value="0"/>```

#### InstallBGDD
If you want to prevent duplicate file finder to be installed, enable this policy and set value 0.

If you don't want to prevent duplicate file finder to be installed, enable this policy and set value 1.

More information [here](https://kb.corel.com/129410).

> [!NOTE]
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<enabled/> <data id="InstallBGDD" value="0"/>```

##### Technical information
- **Friendly name of the setting:** [Applets] Prevent the duplicate file finder from being installed
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Nico Mak Computing\WinZip\Policies
- **Value Type:** REG_SZ
- **Value Name:** InstallBGDD
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that the registry key does not exist. In this case, the application uses the default value that is hardcoded in the application, and the setting is therefore not disabled, even though the registry value no longer exists (or application may re-create default registry value again). If you want to disable the setting via Intune, please ensure that value is then set to ```<enabled/> <data id="InstallBGDD" value="0"/>```

#### NoUpdateChecking
If you want to completely disable "Check for Updates", enable this policy and set value 1.

If you don't want to disable "Check for Updates", enable this policy and set value 0.

More information [here](https://kb.winzip.com/en/130452) and [here](https://stealthpuppy.com/disabling-check-for-winzip-update/).

> [!NOTE]
> - **Important:** Configure this policy to User and Device contexts.
> - If you want to disable the setting via Intune, please make sure that value is then set to ```<enabled/> <data id="NoUpdateChecking" value="0"/>```

##### Technical information
- **Friendly name of the setting:** [Software Updates] Completely disable "Check for Updates"
- **Registry Hive:** HKEY_LOCAL_MACHINE / HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Nico Mak Computing\WinZip\UpdateCheck
- **Value Type:** REG_SZ
- **Value Name:** NoUpdateChecking
- **Enabled Value:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that the registry key does not exist. In this case, the application uses the default value that is hardcoded in the application, and the setting is therefore not disabled, even though the registry value no longer exists (or application may re-create default registry value again). If you want to disable the setting via Intune, please ensure that value is then set to ```<enabled/> <data id="NoUpdateChecking" value="0"/>```