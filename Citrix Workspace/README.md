# Citrix Workspace

This repository includes OMA-URI for Citrix Workspace and some of the common settings that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| [receiver.admx](https://docs.citrix.com/en-us/citrix-workspace-app-for-windows/group-policy) | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/receiver/Policy/receiverAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the common settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```Policy_AutoUpdateVersionControlPolicy``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/receiver~Policy~CITRIX_COMPONENTS~ICAClient~AutoUpdate/Policy_AutoUpdateVersionControlPolicy``` | String | ```<enabled/> <data id="Part_CWA_Version" value=""/> <data id="Part_UpgradeToLatest" value="true"/> <data id="Part_CustomStartDate" value=""/> <data id="Part_DeliveryPeriod" value="0"/>```
| ```Policy_CheckAutoUpdatePolicy``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/receiver~Policy~CITRIX_COMPONENTS~ICAClient~AutoUpdate/Policy_CheckAutoUpdatePolicy``` | String | ```<enabled/> <data id="Part_CheckAutoUpdatePolicy" value="0"/>```
| ```Policy_EnableAutoUpdatePolicy``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/receiver~Policy~CITRIX_COMPONENTS~ICAClient~AutoUpdate/Policy_EnableAutoUpdatePolicy``` | String | ```<enabled/> <data id="Part_EnableAutoUpdatePolicy" value="True"/> <data id="Part_EnableAutoUpdatePolicy_version" value="False"/> <data id="Part_EnableAutoUpdatePolicy_switchArchitecture" value="False"/>```
| ```Policy_Keyboard_Hotkeys``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/receiver~Policy~CITRIX_COMPONENTS~ICAClient~UserExperience/Policy_Keyboard_Hotkeys``` | String | ```<enabled/> <data id="Part_Keyboard_Hotkey_Tasklist" value="Shift"/> <data id="Part_Keyboard_Hotkey_Tasklist_Plus" value="F1"/> <data id="Part_Keyboard_Hotkey_Close_Remote_Application" value="Shift"/> <data id="Part_Keyboard_Hotkey_Close_Remote_Application_Plus" value="F3"/> <data id="Part_Keyboard_Hotkey_Toggle_Title_Bar" value="Shift"/> <data id="Part_Keyboard_Hotkey_Toggle_Title_Bar_Plus" value="F2"/> <data id="Part_Keyboard_Hotkey_Ctrl_Alt_Del" value="Ctrl"/> <data id="Part_Keyboard_Hotkey_Ctrl_Alt_Del_Plus" value="F1"/> <data id="Part_Keyboard_Hotkey_Ctrl_Shift_Esc" value="Ctrl"/> <data id="Part_Keyboard_Hotkey_Ctrl_Shift_Esc_Plus" value="F3"/> <data id="Part_Keyboard_Hotkey_Alt_Tab" value="Alt"/> <data id="Part_Keyboard_Hotkey_Alt_Tab_Plus" value="F8"/> <data id="Part_Keyboard_Hotkey_Alt_Backtab" value="Alt"/> <data id="Part_Keyboard_Hotkey_Alt_Backtab_Plus" value="F9"/> <data id="Part_Keyboard_Hotkey_Ctrl_Esc" value="Ctrl"/> <data id="Part_Keyboard_Hotkey_Ctrl_Esc_Plus" value="F2"/> <data id="Part_Keyboard_Hotkey_Ctrl_Alt" value="Alt"/> <data id="Part_Keyboard_Hotkey_Ctrl_Alt_Plus" value="F2"/> <data id="Part_Keyboard_Hotkey_Toggle_Latency_Reduction" value="Ctrl"/> <data id="Part_Keyboard_Hotkey_Toggle_Latency_Reduction_Plus" value="F5"/> <data id="Part_Keyboard_Hotkey_Toggle_LOCALIME" value="Shift"/> <data id="Part_Keyboard_Hotkey_Toggle_LOCALIME_Plus" value="F4"/> <data id="Part_Keyboard_Hotkey_Toggle_RelativeMouse" value="Ctrl"/> <data id="Part_Keyboard_Hotkey_Toggle_RelativeMouse_Plus" value="F12"/> <data id="Part_Keyboard_Windows_Key" value="Remote"/>```

### Descriptions
More details of the settings can be found this chapter.

#### Policy_AutoUpdateVersionControlPolicy
When enabled, Citrix pushes an automatic update to end users when the Citrix Workspace app is installed. The update can be the latest or a specific version.

More information:
https://docs.citrix.com/en-us/citrix-workspace-app-for-windows/updates#auto-update-version-control

**Examples:**
| Scenario | Value 
|---------|---------|
| Upgrade always to latest version immediately after its release (Recommended). | ```<enabled/> <data id="Part_CWA_Version" value=""/> <data id="Part_UpgradeToLatest" value="true"/> <data id="Part_CustomStartDate" value=""/> <data id="Part_DeliveryPeriod" value="0"/>``` |
| Upgrade always to latest version but preferred delivery period delay is 2 days. |```<enabled/> <data id="Part_CWA_Version" value=""/> <data id="Part_UpgradeToLatest" value="true"/> <data id="Part_CustomStartDate" value=""/> <data id="Part_DeliveryPeriod" value="2"/>``` |
| Upgrade to app version 14.10.1.5 and preferred start date is 27 November 2024. | ```<enabled/> <data id="Part_CWA_Version" value="24.10.1.5"/> <data id="Part_UpgradeToLatest" value="false"/> <data id="Part_CustomStartDate" value="2024-11-27"/> <data id="Part_DeliveryPeriod" value="0"/>```  |

##### Technical information (deliveryPeriod)
- **Friendly name of the setting:** Worksapce app version > Preferred Delivery Period
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate\1CDF566D-B2C7-47CA-802F-6283C862E1D6
- **Value Type:** REG_SZ
- **Value Name:** deliveryPeriod
- **Enabled Value:** 0
- **Disabled Value:** N/A

##### Technical information (startDate)
- **Friendly name of the setting:** Worksapce app version > Preferred Start Date
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate\1CDF566D-B2C7-47CA-802F-6283C862E1D6
- **Value Type:** REG_SZ
- **Value Name:** startDate
- **Enabled Value:** ``` ```
- **Disabled Value:** N/A

##### Technical information (UpgradeToLatest)
- **Friendly name of the setting:** Worksapce app version > Upgrade To Latest Version
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate\1CDF566D-B2C7-47CA-802F-6283C862E1D6
- **Value Type:** REG_DWORD
- **Value Name:** startDate
- **Enabled Value:** 1
- **Disabled Value:** N/A

##### Technical information (versionControl)
- **Friendly name of the setting:** Worksapce app version > Workspace App Version
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate\1CDF566D-B2C7-47CA-802F-6283C862E1D6
- **Value Type:** REG_SZ
- **Value Name:** versionControl
- **Enabled Value:** ``` ```
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Policy_CheckAutoUpdatePolicy
This policy is used to set the preference when the Citrix Workspace-update is rolled-out to the users.

| Preference | Value | Description
|---------|---------|---------|
| Fast (Recommended) | ```<data id="Part_CheckAutoUpdatePolicy" value="0"/>``` |  Available updates are rolled-out to the users at the beginning of delivery period.
| Medium | ```<data id="Part_CheckAutoUpdatePolicy" value="4"/>```  | Available updates are rolled-out to the users at mid-delivery period.
| Slow | ```<data id="Part_CheckAutoUpdatePolicy" value="9"/>```  | Available updates are rolled-out to the users at the end of delivery period.

More information:
https://docs.citrix.com/en-us/citrix-workspace-app-for-windows/updates#configure-the-delay-in-checking-for-updates

##### Technical information
- **Friendly name of the setting:** Set the Delay in Checking for Update
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate
- **Value Type:** REG_SZ
- **Value Name:** BucketId
- **Enabled Value (Fast):** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Policy_EnableAutoUpdatePolicy
Not Configured – Citrix Workspace Updates is enabled.<br>
Enabled – Citrix Workspace Updates is enabled with the additional options listed in this dialog.<br>
Disabled – Citrix Workspace Updates option is hidden from the Advanced Preferences sheet and you will not receive any update notifications.

*Enable Citrix Workspace Update Policy:*
| Preference | Value | Description
|---------|---------|---------|
| Auto (Recommended) | ```<data id="Part_EnableAutoUpdatePolicy" value="True"/>``` |  Citrix Workspace checks for updates automatically.
| Manual | ```<data id="Part_EnableAutoUpdatePolicy" value="False"/>``` | User checks for updates manually. 


*LTSR ONLY:*
| Preference | Value | Description
|---------|---------|---------|
| True | ```<data id="Part_EnableAutoUpdatePolicy_version" value="True"/>``` |Only LTSR updates will be available.
| False (Recommended) | ```<data id="Part_EnableAutoUpdatePolicy_version" value="False"/>``` |All updates will be available.

*Migrate 32-bit application to system processir architecture (64-bit or ARM64):*
| Preference | Value | Description
|---------|---------|---------|
| True | ```<data id="Part_EnableAutoUpdatePolicy_switchArchitecture" value="True"/>``` |The auto-updates upgrade Citrix Workspace from 32-bit to match the system processor architecture (64-bit or ARM64).
| False (Recommended) | ```<data id="Part_EnableAutoUpdatePolicy_switchArchitecture" value="False"/>``` |Updates keep the current architecture. **This is the default value.**

More information:
- https://docs.citrix.com/en-us/citrix-workspace-app-for-windows/updates#configure-the-delay-in-checking-for-updates
- https://docs.citrix.com/en-us/citrix-workspace-app-for-windows/transition-to-64-bit-faq

##### Technical information (Part_EnableAutoUpdatePolicy)
- **Friendly name of the setting:** Citrix Workspace Updates > Enable Citrix Workspace Update Policy
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate
- **Value Type:** REG_SZ
- **Value Name:** Enable
- **Enabled Value (Fast):** True
- **Disabled Value:** N/A

##### Technical information (Part_EnableAutoUpdatePolicy_version)
- **Friendly name of the setting:** Citrix Workspace Updates > LTSR ONLY
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate
- **Value Type:** REG_SZ
- **Value Name:** LTSROnly
- **Enabled Value (Fast):** False
- **Disabled Value:** N/A

##### Technical information (Part_EnableAutoUpdatePolicy_switchArchitecture)
- **Friendly name of the setting:** Migrate 32-bit application to system processir architecture (64-bit or ARM64)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\AutoUpdate
- **Value Type:** REG_SZ
- **Value Name:** MigrateCWAArchitecture
- **Enabled Value (False):** False
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Policy_Keyboard_Hotkeys
This option enables configuring key combinations that the Citrix Workspace can use.

From the Windows Key drop down menu, select the preferred option. The available options are Access Local Desktop, Access Remote Session and Access Remote session in full screen only. 

*Windows key:*
| Preference | Value | Description
|---------|---------|---------|
| Access Local Desktop | ```<data id="Part_Keyboard_Windows_Key" value="Local"/>``` |  When Access Local Desktop is selected, the key combination is applicable only to the local desktop.
| Access Remote Session (Recommeded) | ```<data id="Part_Keyboard_Windows_Key" value="Remote"/>``` | When Access Remote Session is selected, the key combination is applicable only to the remote session. 
| Access Remote Session in full-screen only | ```<data id="Part_Keyboard_Windows_Key" value="FullScreenOnly"/>``` | When Access Remote session in full screen only is selected, the key combination is applicable to non-seamless ICA sessions in full screen mode. By default, this option is selected. 

More information and keyboard shortcuts:
https://docs.citrix.com/en-us/citrix-workspace-app-for-windows/keyboard.html

##### Technical information (Part_Keyboard_Windows_Key)
- **Friendly name of the setting:** Keyboard Shortcuts > Windows key
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\Engine\Lockdown Profiles\All Regions\Lockdown\Virtual Channels\Keyboard
- **Value Type:** REG_SZ
- **Value Name:** TransparentKeyPassthrough
- **Enabled Value (Access Remote Session)** Remote
- **Disabled Value:** N/A

##### Technical information (Part_Keyboard_Hotkey_< Function >)
- **Friendly name of the setting:** Keyboard Shortcuts > Task List/Close Application/Toggle Full-screen/Ctrl-Alt-Del/Task Manager/Alt-Tab/Alt-Shift-Tab/Ctrl-Esc/Ctrl-Alt/Latency Reduction/Generic IME Mode/Relative Mouse
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Citrix\ICA Client\Engine\Lockdown Profiles\All Regions\Lockdown\Client Engine\Hot Keys
- **Value Type:** REG_SZ
- **Value Name:** HotKeyXXChar / HotKeyXXShift
- **Enabled Value:** < Keyboard Shortcut Value >
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.