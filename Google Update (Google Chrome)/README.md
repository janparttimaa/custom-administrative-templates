# Google Update (Google Chrome)

This repository includes OMA-URI for Google Update (Google Chrome) and some of the common settings that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| [GoogleUpdate.admx](https://chromeenterprise.google/?modal-id=download-chrome#management-download) | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/GoogleUpdate/Policy/GoogleUpdateAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the common settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

> [!NOTE]  
> As an example, we will only show some few common settings and their OMA-URI values.

| Name | Description | OMA-URI | Data type | Recommended Value |
|---------|---------|---------|---------|---------|
| ```Pol_AllowInstallationGoogleChrome``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChrome/Pol_AllowInstallationGoogleChrome``` | String | ```<enabled/><data id="Part_InstallPolicy" value="1"/>``` |
| ```Pol_AllowInstallationGoogleChromeBeta``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChromeBeta/Pol_AllowInstallationGoogleChromeBeta``` | String | ```<enabled/><data id="Part_InstallPolicy" value="0"/>``` |
| ```Pol_AllowInstallationGoogleChromeCanaryBuild``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChromeCanaryBuild/Pol_AllowInstallationGoogleChromeCanaryBuild``` | String | ```<enabled/><data id="Part_InstallPolicy" value="0"/>``` |
| ```Pol_AllowInstallationGoogleChromeDev``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChromeDev/Pol_AllowInstallationGoogleChromeDev``` | String | ```<enabled/><data id="Part_InstallPolicy" value="0"/>``` |
| ```Pol_AutoUpdateCheckPeriod``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Preferences/Pol_AutoUpdateCheckPeriod``` | String | ```<enabled/><data id="Part_AutoUpdateCheckPeriod" value="240"/>``` |
| ```Pol_DefaultUpdatePolicy``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications/Pol_DefaultUpdatePolicy``` | String | ```<enabled/><data id="Part_UpdatePolicy" value="1"/>``` |
| ```Pol_ProxyMode``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_ProxyServer/Pol_ProxyMode``` | String | ```<enabled/><data id="Part_ProxyMode" value="direct"/>``` |
| ```Pol_UpdatePolicyGoogleChrome``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChrome/Pol_UpdatePolicyGoogleChrome``` | String | ```<enabled/><data id="Part_UpdatePolicy" value="1"/>``` |
| ```Pol_UpdatePolicyGoogleChromeBeta``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChromeBeta/Pol_UpdatePolicyGoogleChromeBeta``` | String | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>``` |
| ```Pol_UpdatePolicyGoogleChromeCanaryBuild``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChromeCanaryBuild/Pol_UpdatePolicyGoogleChromeCanaryBuild``` | String | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>``` |
| ```Pol_UpdatePolicyGoogleChromeDev``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChromeDev/Pol_UpdatePolicyGoogleChromeDev``` | String | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>``` |
| ```Pol_TargetChannelGoogleChrome``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/GoogleUpdate~Policy~Cat_GoogleUpdate~Cat_Applications~Cat_GoogleChrome/Pol_TargetChannelGoogleChrome``` | String | ```<enabled/><data id="Part_TargetChannel" value="stable"/>``` |

### Descriptions
More details of the settings can be found this chapter.

#### Pol_AllowInstallationGoogleChrome
Specifies whether Google Chrome can be installed using Google Update/Google Installer.

If this policy is not configured, Google Chrome can be installed as specified by "Allow installation default".

Force Installs (Machine-Wide): Allows Deploying Google Chrome to all machines where Google Update is pre-installed. Requires Google Update 1.3.36.82 or higher.

Force Installs (Per-User): Allows Deploying Google Chrome on a Per-User basis to all machines where Google Update is pre-installed Per-User. Requires Google Update 1.3.36.82 or higher.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Option | Value 
|---------|---------|
| Always allow Installs (recommended) | ```<enabled/><data id="Part_InstallPolicy" value="1"/>``` |
| Always allow Machine-Wide Installs, but not Per-User Installs.|```<enabled/><data id="Part_InstallPolicy" value="4"/>``` |
| Force Installs (Machine-Wide) | ```<enabled/><data id="Part_InstallPolicy" value="5"/>```  |
| Force Installs (Per-User) | ```<enabled/><data id="Part_InstallPolicy" value="6"/>```  |
| Installs disabled | ```<enabled/><data id="Part_InstallPolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Allow installation (Google Chrome)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Install{8A69D345-D564-463C-AFF1-A69D9E530F96}
- **Enabled Value:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_AllowInstallationGoogleChromeBeta
Specifies whether Google Chrome Beta can be installed using Google Update/Google Installer.

If this policy is not configured, Google Chrome Beta can be installed as specified by "Allow installation default".

Force Installs (Machine-Wide): Allows Deploying Google Chrome Beta to all machines where Google Update is pre-installed. Requires Google Update 1.3.36.82 or higher.

Force Installs (Per-User): Allows Deploying Google Chrome Beta on a Per-User basis to all machines where Google Update is pre-installed Per-User. Requires Google Update 1.3.36.82 or higher.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

| Option | Value 
|---------|---------|
| Always allow Installs (recommended) | ```<enabled/><data id="Part_InstallPolicy" value="1"/>``` |
| Always allow Machine-Wide Installs, but not Per-User Installs.|```<enabled/><data id="Part_InstallPolicy" value="4"/>``` |
| Force Installs (Machine-Wide) | ```<enabled/><data id="Part_InstallPolicy" value="5"/>```  |
| Force Installs (Per-User) | ```<enabled/><data id="Part_InstallPolicy" value="6"/>```  |
| Installs disabled | ```<enabled/><data id="Part_InstallPolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Allow installation (Google Chrome Beta)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Install{8237E44A-0054-442C-B6B6-EA0509993955}
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_AllowInstallationGoogleChromeCanaryBuild
Specifies whether Google Chrome Canary Build can be installed using Google Update/Google Installer.

If this policy is not configured, Google Chrome Canary Build can be installed as specified by "Allow installation default".

Force Installs (Machine-Wide): Allows Deploying Google Chrome Canary Build to all machines where Google Update is pre-installed. Requires Google Update 1.3.36.82 or higher.

Force Installs (Per-User): Allows Deploying Google Chrome Canary Build on a Per-User basis to all machines where Google Update is pre-installed Per-User. Requires Google Update 1.3.36.82 or higher.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Option | Value 
|---------|---------|
| Always allow Installs (recommended) | ```<enabled/><data id="Part_InstallPolicy" value="1"/>``` |
| Always allow Machine-Wide Installs, but not Per-User Installs.|```<enabled/><data id="Part_InstallPolicy" value="4"/>``` |
| Force Installs (Machine-Wide) | ```<enabled/><data id="Part_InstallPolicy" value="5"/>```  |
| Force Installs (Per-User) | ```<enabled/><data id="Part_InstallPolicy" value="6"/>```  |
| Installs disabled | ```<enabled/><data id="Part_InstallPolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Allow installation (Google Chrome Canary Build)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Install{4EA16AC7-FD5A-47C3-875B-DBF4A2008C20}
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_AllowInstallationGoogleChromeDev
Specifies whether Google Chrome Dev can be installed using Google Update/Google Installer.

If this policy is not configured, Google Chrome Dev can be installed as specified by "Allow installation default".

Force Installs (Machine-Wide): Allows Deploying Google Chrome Dev to all machines where Google Update is pre-installed. Requires Google Update 1.3.36.82 or higher.

Force Installs (Per-User): Allows Deploying Google Chrome Dev on a Per-User basis to all machines where Google Update is pre-installed Per-User. Requires Google Update 1.3.36.82 or higher.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Option | Value 
|---------|---------|
| Always allow Installs (recommended) | ```<enabled/><data id="Part_InstallPolicy" value="1"/>``` |
| Always allow Machine-Wide Installs, but not Per-User Installs.|```<enabled/><data id="Part_InstallPolicy" value="4"/>``` |
| Force Installs (Machine-Wide) | ```<enabled/><data id="Part_InstallPolicy" value="5"/>```  |
| Force Installs (Per-User) | ```<enabled/><data id="Part_InstallPolicy" value="6"/>```  |
| Installs disabled | ```<enabled/><data id="Part_InstallPolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Allow installation (Google Chrome Dev)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Install{401C381F-E0DE-4B85-8BD8-3F3F14FBDA57}
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_AutoUpdateCheckPeriod
Minimum number of minutes between automatic update checks.

Set this policy to the value 0 to disable all periodic network traffic by Google Update. This is not recommended, as it prevents Google Update itself from receiving stability and security updates.

The "Update policy override default" and per-application "Update policy override" settings should be used to manage application updates rather than this setting.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Cdefault-policies-preferences

##### Technical information
- **Friendly name of the setting:** Auto-update check period override
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** AutoUpdateCheckPeriodMinutes
- **Enabled Value:** 240
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_DefaultUpdatePolicy
Specifies the default policy for software updates from Google.

Can be overridden by the "Update policy override" for individual applications.

Options:
 - Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
 - Manual updates only: Updates are only applied when the user does a manual update check. (Not all apps provide an interface for this.)
 - Automatic silent updates only: Updates are only applied when they are found via the periodic update check.
 - Updates disabled: Never apply updates.

If you select manual updates, you should periodically check for updates using each application's manual update mechanism if available. If you disable updates, you should periodically check for updates and distribute them to users.

Only affects updates for Google software that uses Google Update for updates. Does not prevent auto-updates of Google software that does not use Google Update for updates.

Updates for Google Update are not affected by this setting; Google Update will continue to update itself while it is installed.

WARNING: Disabing updates will also prevent updates of any new Google applications released in the future, possibly including dependencies for future versions of installed applications.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

**Examples:**
| Option | Value 
|---------|---------|
| Always allow updates (recommended)| ```<enabled/><data id="Part_UpdatePolicy" value="1"/>``` |
| Manual updates only |```<enabled/><data id="Part_UpdatePolicy" value="2"/>``` |
| Automatic silent updates only | ```<enabled/><data id="Part_UpdatePolicy" value="3"/>```  |
| Updates disabled | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>```  |

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Cdefault-policies-preferences%2Capp-policies

##### Technical information
- **Friendly name of the setting:** Update policy override default
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** UpdateDefault
- **Enabled Value:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_ProxyMode
Allows you to specify the proxy server used by Google Update.

If you choose to never use a proxy server and always connect directly, all other options are ignored.

If you choose to use system proxy settings or auto detect the proxy server, all other options are ignored.

If you choose fixed server proxy mode, you can specify further options in 'Address or URL of proxy server'.

If you choose to use a .pac proxy script, you must specify the URL to the script in 'URL to a proxy .pac file'.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

**Examples:**
| Option | Value 
|---------|---------|
| Auto detect proxy settings| ```<enabled/><data id="Part_ProxyMode" value="auto_detect"/>``` |
| Never use a proxy |```<enabled/><data id="Part_ProxyMode" value="direct"/>``` |
| Use a .pac proxy script | ```<enabled/><data id="Part_ProxyMode" value="pac_script"/>```  |
| Use fixed proxy servers | ```<enabled/><data id="Part_ProxyMode" value="fixed_servers"/>```  |
| Use system proxy settings | ```<enabled/><data id="Part_ProxyMode" value="system"/>```  |

##### Technical information
- **Friendly name of the setting:** Choose how to specify proxy server settings
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_SZ
- **Value Name:** ProxyMode
- **Enabled Value:** direct
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_UpdatePolicyGoogleChrome
Specifies how Google Update handles available Google Chrome updates from Google.

If this policy is not configured, Google Update handles available updates as specified by "Update policy override default".

Options:
 - Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
 - Manual updates only: Updates are only applied when the user does a manual update check. (Not all apps provide an interface  for this.)
 - Automatic silent updates only: Updates are only applied when they are found via the periodic update check.
 - Updates disabled: Never apply updates.

If you select manual updates, you should periodically check for updates using the application's manual update mechanism if available. If you disable updates, you should periodically check for updates and distribute them to users. Check https://www.google.com/chrome/.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Option | Value 
|---------|---------|
| Always allow updates (recommended)| ```<enabled/><data id="Part_UpdatePolicy" value="1"/>``` |
| Manual updates only |```<enabled/><data id="Part_UpdatePolicy" value="2"/>``` |
| Automatic silent updates only | ```<enabled/><data id="Part_UpdatePolicy" value="3"/>```  |
| Updates disabled | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Update policy override (Google Chrome)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Update{8A69D345-D564-463C-AFF1-A69D9E530F96}
- **Enabled Value:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_UpdatePolicyGoogleChromeBeta
Specifies how Google Update handles available Google Chrome Beta updates from Google.

If this policy is not configured, Google Update handles available updates as specified by "Update policy override default".

Options:
 - Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
 - Manual updates only: Updates are only applied when the user does a manual update check. (Not all apps provide an interface  for this.)
 - Automatic silent updates only: Updates are only applied when they are found via the periodic update check.
 - Updates disabled: Never apply updates.

If you select manual updates, you should periodically check for updates using the application's manual update mechanism if available. If you disable updates, you should periodically check for updates and distribute them to users. Check https://www.google.com/chrome/browser/beta.html.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Option | Value 
|---------|---------|
| Always allow updates (recommended)| ```<enabled/><data id="Part_UpdatePolicy" value="1"/>``` |
| Manual updates only |```<enabled/><data id="Part_UpdatePolicy" value="2"/>``` |
| Automatic silent updates only | ```<enabled/><data id="Part_UpdatePolicy" value="3"/>```  |
| Updates disabled | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Update policy override (Google Chrome Beta)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Update{8237E44A-0054-442C-B6B6-EA0509993955}
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_UpdatePolicyGoogleChromeCanaryBuild
Specifies how Google Update handles available Google Chrome Canary Build updates from Google.

If this policy is not configured, Google Update handles available updates as specified by "Update policy override default".

Options:
 - Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
 - Manual updates only: Updates are only applied when the user does a manual update check. (Not all apps provide an interface  for this.)
 - Automatic silent updates only: Updates are only applied when they are found via the periodic update check.
 - Updates disabled: Never apply updates.

If you select manual updates, you should periodically check for updates using the application's manual update mechanism if available. If you disable updates, you should periodically check for updates and distribute them to users. Check https://www.google.com/chrome/browser/canary.html.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Option | Value 
|---------|---------|
| Always allow updates (recommended)| ```<enabled/><data id="Part_UpdatePolicy" value="1"/>``` |
| Manual updates only |```<enabled/><data id="Part_UpdatePolicy" value="2"/>``` |
| Automatic silent updates only | ```<enabled/><data id="Part_UpdatePolicy" value="3"/>```  |
| Updates disabled | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Update policy override (Google Chrome Canary Build)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Update{4EA16AC7-FD5A-47C3-875B-DBF4A2008C20}
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_UpdatePolicyGoogleChromeDev
Specifies how Google Update handles available Google Chrome Dev updates from Google.

If this policy is not configured, Google Update handles available updates as specified by "Update policy override default".

Options:
 - Always allow updates: Updates are always applied when found, either by periodic update check or by a manual update check.
 - Manual updates only: Updates are only applied when the user does a manual update check. (Not all apps provide an interface  for this.)
 - Automatic silent updates only: Updates are only applied when they are found via the periodic update check.
 - Updates disabled: Never apply updates.

If you select manual updates, you should periodically check for updates using the application's manual update mechanism if available. If you disable updates, you should periodically check for updates and distribute them to users. Check https://www.google.com/chrome/browser/index.html?extra=devchannel

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Option | Value 
|---------|---------|
| Always allow updates (recommended)| ```<enabled/><data id="Part_UpdatePolicy" value="1"/>``` |
| Manual updates only |```<enabled/><data id="Part_UpdatePolicy" value="2"/>``` |
| Automatic silent updates only | ```<enabled/><data id="Part_UpdatePolicy" value="3"/>```  |
| Updates disabled | ```<enabled/><data id="Part_UpdatePolicy" value="0"/>```  |

##### Technical information
- **Friendly name of the setting:** Update policy override (Google Chrome Dev)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_DWORD
- **Value Name:** Update{401C381F-E0DE-4B85-8BD8-3F3F14FBDA57}
- **Enabled Value:** 0
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### Pol_TargetChannelGoogleChrome
Specifies which Channel Google Chrome should be updated to.

When this policy is enabled, the app will be updated to the Channel with this policy value.

Some examples:
1) Not configured: app will be updated to the latest version available in the default Channel for the app.
2) Policy value is set to "stable": the app will be updated to the latest stable version.
3) Policy value is set to "beta": the app will be updated to the latest beta version.
4) Policy value is set to "dev": the app will be updated to the latest dev version.

This policy is available only on Windows instances that are joined to a Microsoft&#x00AE; Active Directory&#x00AE; domain.

More information:
https://support.google.com/chrome/a/answer/6350036?hl=en#zippy=%2Cget-the-google-update-policy-template%2Capp-policies

**Examples:**
| Channel | Value 
|---------|---------|
| stable| ```<enabled/><data id="Part_TargetChannel" value="stable"/>``` |
| beta |```<enabled/><data id="Part_TargetChannel" value="beta"/>``` |
| dev | ```<enabled/><data id="Part_TargetChannel" value="dev"/>```  |

##### Technical information
- **Friendly name of the setting:** Target Channel override (Google Chrome)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Google\Update
- **Value Type:** REG_SZ
- **Value Name:** TargetChannel{8A69D345-D564-463C-AFF1-A69D9E530F96}
- **Enabled Value:** stable
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.