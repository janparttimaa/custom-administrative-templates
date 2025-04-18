# WinSCP

This repository includes custom Administrative Templates for WinSCP that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| WinSCP | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/WinSCP/Policy/WinSCPAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Possible Values
|---------|---------|---------|---------|---------|
| ```BetaVersions``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/WinSCP~Policy~WinSCP/BetaVersions``` | String | ```<enabled/> <data id="BetaVersions_Dropdown" value="2"/>```<br><br>```<enabled/> <data id="BetaVersions_Dropdown" value="1"/>```<br><br>```<enabled/> <data id="BetaVersions_Dropdown" value="0"/>```<br><br>```<disabled/>```
| ```Period``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/WinSCP~Policy~WinSCP/Period``` | String | ```<enabled/> <data id="Period_Dropdown" value="0"/>```<br><br>```<enabled/> <data id="Period_Dropdown" value="1"/>```<br><br>```<enabled/> <data id="Period_Dropdown" value="7"/>```<br><br>```<enabled/> <data id="Period_Dropdown" value="30"/>```<br><br>```<disabled/>```
| ```ShowOnStartup``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/WinSCP~Policy~WinSCP/ShowOnStartup``` | String | ```<enabled/>```<br><br>```<disabled/>```

### Descriptions
More details of the settings can be found this chapter.

#### BetaVersions
Set and enforce setting "Check for beta versions" of the WinSCP.

If you want to check beta versions of the WinSCP or makes sure that checking beta versions are entirely disabled, enable this policy and choose preferred value. If user change the preferred setting and value from WinSCP's settings, setting and value will be enforced back to be preffered setting and value next time when device's policy refresh cycle starts.

- Value "Auto" makes WinSCP check for beta releases, only if you ever have used any beta release before. This option is available in stable releases only. Beta releases report newer beta releases always. 
- Value "Off" disables check for beta releases. If you are centrally mass deploying WinSCP using e.g. Microsoft Intune or Configuration Manager, you should choose this setting. This is also recommended setting if you don't want to use beta releases.
- Value "On" enables check for beta releases.

Here are these values translated to numeric values for Intune-deployment:

| Value (GPO) | Value (Intune) |
|---------|---------|
| Auto | 2 |
| Off | 1 |
| On | 0 |

If you disable or not configure this setting, user can choose preferred choice from WinSCP's settings and we will not enforce user to use specific value of the setting.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** [Updates] Check for beta versions
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Martin Prikyl\WinSCP 2\Configuration\Interface\Updates
- **Value Type:** REG_DWORD
- **Value Name:** BetaVersions
- **Enabled Values:**
    - **Auto:** 2
    - **Off:** 1
    - **On:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Period
If you want to set automatic update period, enable this policy and set prefferred period. If user changes preferred period to something else from WinSCP's settings, period will be enforced back to preferred period next time when device's policy refresh cycle starts.

- Value "Never" disables automatic update check. If you are centrally mass deploying WinSCP using e.g. Microsoft Intune or Configuration Manager, you should enable and choose this setting.
- Value "Daily" checks updates once per day.
- Value "Weekly" checks updates once per week.
- Value "Monthly" checks updates once per month.

Here are these values translated to numeric values for Intune-deployment:

| Value (GPO) | Value (Intune) |
|---------|---------|
| Never | 0 |
| Daily | 1 |
| Weekly | 7 |
| Monthly | 30 |

If you disable or not configure this setting, user can choose preferred period from WinSCP's settings and we will not enforce user to use specific period.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** [Updates] Automatic check period
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Martin Prikyl\WinSCP 2\Configuration\Interface\Updates
- **Value Type:** REG_DWORD
- **Value Name:** Period
- **Enabled Values:**
    - **None:** 0
    - **Daily:** 1
    - **Weekly:** 7
    - **Monthly:** 30
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### ShowOnStartup
If you want to display information about pending software update on the startup of WinSCP, enable this policy. If user disbales the setting from WinSCP's settings, setting will be enforced back to be enabled next time when device's policy refresh cycle starts.

If you disable this setting, user cannot see pending software update on the startup of WinSCP.  If you are centrally mass deploying WinSCP using e.g. Microsoft Intune or Configuration Manager, you should disable this setting.

If you not configure this setting, user can choose preferred choice from WinSCP's settings and we will not enforce user to use specific value of the setting.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** [Updates] Display information about update on startup
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Martin Prikyl\WinSCP 2\Configuration\Interface\Updates
- **Value Type:** REG_DWORD
- **Value Name:** ShowOnStartup
- **Enabled Value:** 1
- **Disabled Value:** 0
