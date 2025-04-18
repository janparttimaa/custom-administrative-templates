# iManage

This repository includes custom Administrative Templates for iManage that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-templates
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| iManage | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/iManage/Policy/iManageAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```Auto Download Update``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/iManage~Policy~iManage/AutoDownloadUpdate``` | String | ```<enabled/>```
| ```Selected Update Channel``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/iManage~Policy~iManage/SelectedUpdateChannel``` | String | ```<enabled/> <data id="SelectedUpdateChannel" value="release"/>```

> [!NOTE]  
> iManage mandates, that following additional settings needs to be configured, especially when using iManage Drive: <br><br>
> <kbd><img src= "../img/iManageAdditionalSettings.png" alt="Screenshot from Microsoft Intune of additional settings for iManage"> </kbd>

### Descriptions
More details of the settings can be found this chapter.

#### Auto Download Update
You can specify whether updates should be downloaded and installed automatically. This setting ensures that if there are any updates, they're automatically downloaded and installed on the user's device. This provides a seamless and quicker installation experience for users.

If you enable this policy, The "Automatically download and install updates" option is selected by default on the "Update Settings" screen of iManage Agent Services and users cannot disable it.

If you not configure this setting, user can manage itself this setting adn we are not managing or enforcing it.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Automatically download and install updates
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\iManage\WorkAgent\AutoUpdate
- **Value Type:** REG_DWORD
- **Value Name:** Auto Download Update
- **Enabled Value:** 1
- **Disabled Value:** 0

#### Selected Update Channel
Setting auto update channel to iManage.

iManage Work Agent provides the ability to switch between the update channels. Depending on how they are configured in your environment, you may be able to see and select different update channels. To use this feature and select preferred update channel to all users, enable this policy and select preferred update channel.

Please check available values for auto update channel in this table below:
<br>_(List updated 5 April 2025)_

| Channel | Value | More information
|---------|---------|---------|
| Release Work 10 / Release Work 10 with Drive | ```release``` | **<li> This is recommended channel.**<br><li> This channel is supported to iManage Work 10 and iManage Drive. |
| Coming Soon Work 10 / Coming Soon Work 10 with Drive | ```coming_soon``` | <li> This channel is supported to iManage Work 10 and iManage Drive.  |
| Release Work 10 with DeskSite | ```release_compatibility``` | <li> This channel is only supported to iManage Work 10.  |
| Release Work 10 with FileSite | ```release_compatibility_fs``` | <li> This channel is only supported to iManage Work 10.  |
| Release Work 10.7.1 | ```release_1071``` | <li> This channel is only supported to iManage Work 10.  |
| Coming Soon Work 10 with DeskSite | ```coming_soon_compatibility``` | <li> This channel is only supported to iManage Work 10.  |
| Coming Soon Work 10 with FileSite | ```coming_soon_compatibility_fs``` | <li> This channel is only supported to iManage Work 10. |

If you disable or not configuring this setting, user can itself select preferred update channel from iManage Work Agent settings.

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Automatically download and install updates
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\iManage\AgentServices\AutoUpdate
- **Value Type:** REG_SZ
- **Value Name:** Selected Update Channel
- **Enabled Values:**
    - **Release Work 10 / Release Work 10 with Drive:** release
    - **Coming Soon Work 10 / Coming Soon Work 10 with Drive:** coming_soon
    - **Release Work 10 with DeskSite:** release_compatibility
    - **Release Work 10 with FileSite:** release_compatibility_fs
    - **Release Work 10.7.1:** release_1071
    - **Coming Soon Work 10 with DeskSite:** coming_soon_compatibility
    - **Coming Soon Work 10 with FileSite:** coming_soon_compatibility_fs
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.