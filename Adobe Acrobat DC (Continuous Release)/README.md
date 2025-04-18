# Adobe Acrobat DC (Continuous Release)

This repository includes custom Administrative Templates for Adobe Acrobat DC (Continuous Release) that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-templates
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Adobe Acrobat DC (Continuous Release) | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/AdobeAcrobatDC/Policy/AdobeAcrobatDCAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

### Preferences
| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```bShowKeyboardSelectionCursor``` | [See below](#bShowKeyboardSelectionCursor) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_Accessibility/bShowKeyboardSelectionCursor``` | String | ```<enabled/>```
| ```bLastAttachLinkMode``` | [See below](#bLastAttachLinkMode) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_EmailAccounts/bLastAttachLinkMode``` | String | ```<enabled/>```
| ```bAutoFill``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_Forms/bAutoFill``` | String | ```<enabled/>```
| ```bRuntimeHighlight``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_Forms/bRuntimeHighlight``` | String | ```<enabled/>```
| ```bBoxConnectorEnabled``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bBoxConnectorEnabled``` | String | ```<enabled/>```
| ```bDisablePDFHandlerSwitching``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bDisablePDFHandlerSwitching``` | String | ```<enabled/>```
| ```bDisableSharePointFeatures``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bDisableSharePointFeatures``` | String | ```<enabled/>```
| ```bDisplayAboutDialog``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bDisplayAboutDialog``` | String | ```<enabled/>```
| ```bDropboxConnectorEnabled``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bDropboxConnectorEnabled``` | String | ```<enabled/>```
| ```bEnableAV2Enterprise``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bEnableAV2Enterprise``` | String | ```<enabled/>```
| ```bGoogleDriveConnectorEnabled``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bGoogleDriveConnectorEnabled``` | String | ```<enabled/>```
| ```bOneDriveConnectorEnabled``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bOneDriveConnectorEnabled``` | String | ```<enabled/>```
| ```bShowMsgAtLaunch``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bShowMsgAtLaunch``` | String | ```<enabled/>```
| ```bSuppressSignOut``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bSuppressSignOut``` | String | ```<enabled/>```
| ```bToggleAdobeDocumentServices``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleAdobeDocumentServices``` | String | ```<enabled/>```
| ```bToggleAdobeSign``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleAdobeSign``` | String | ```<enabled/>```
| ```bToggleFTE``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleFTE``` | String | ```<enabled/>```
| ```bToggleManageSign``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleManageSign``` | String | ```<enabled/>```
| ```bToggleNotifications``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleNotifications``` | String | ```<enabled/>```
| ```bTogglePrefsSync``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bTogglePrefsSync``` | String | ```<enabled/>```
| ```bToggleSendACopy``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleSendACopy``` | String | ```<enabled/>```
| ```bToggleShareFeedback``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleShareFeedback``` | String | ```<enabled/>```
| ```bToggleWebConnectors``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bToggleWebConnectors``` | String | ```<enabled/>```
| ```bWhatsNewExp``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_General/bWhatsNewExp``` | String | ```<enabled/>```
| ```bEnableJS``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_JavaScript/bEnableJS``` | String | ```<enabled/>```
| ```bMIPCheckPolicyOnDocSave``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_Security~Cat_MicrosoftPurviewInformationProtection/bMIPCheckPolicyOnDocSave``` | String | ```<enabled/>```
| ```bMIPLabelling``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_Security~Cat_MicrosoftPurviewInformationProtection/bMIPLabelling``` | String | ```<enabled/>```
| ```bAskBeforeInstalling``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_Security/bAskBeforeInstalling``` | String | ```<enabled/>```
| ```bEnableCertificateBasedTrust``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_SecurityEnhanced/bEnableCertificateBasedTrust``` | String | ```<enabled/>```
| ```bEnhancedSecurityInBrowser``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_SecurityEnhanced/bEnhancedSecurityInBrowser``` | String | ```<enabled/>```
| ```bEnhancedSecurityStandalone``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_SecurityEnhanced/bEnhancedSecurityStandalone``` | String | ```<enabled/>```
| ```bProtectedMode``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_SecurityEnhanced/bProtectedMode``` | String | ```<enabled/>```
| ```bTrustCertifiedDocuments``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_SecurityEnhanced/bTrustCertifiedDocuments``` | String | ```<enabled/>```
| ```bTrustOSTrustedSites``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_SecurityEnhanced/bTrustOSTrustedSites``` | String | ```<enabled/>```
| ```iProtectedView``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_SecurityEnhanced/iProtectedView``` | String | ```<enabled/>```
| ```bAllowOpenFile``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_TrustManager\bAllowOpenFile``` | String | ```<enabled/>```
| ```bLoadSettingsFromURL``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_TrustManager\bLoadSettingsFromURL``` | String | ```<enabled/>```
| ```bUpdater``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_Preferences~Cat_UpdaterAndHelp/bUpdater``` | String | ```<enabled/>```

### Next Generation Licensing (NGL)
| Name | Description | OMA-URI | Data type | Recommended Value 
|---------|---------|---------|---------|---------|
| ```EnableExternalBrowserAuth``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_NGL/EnableExternalBrowserAuth``` | String | ```<enabled/>```
| ```login_domain``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/AdobeAcrobatDC~Policy~Cat_Adobe_Acrobat_DC~Cat_NGL/login_domain``` | String | ```<enabled/>```

### Descriptions
More details of the settings can be found this chapter.

#### bShowKeyboardSelectionCursor
Specifies whether the keyboard selection cursor should always be active in the document. Select this option if you use a screen magnifier.

Possible values:
- Enabled: Always show the cursor.
- Disabled: Don't show the cursor.

GUI mapping:
Edit &gt; Preferences &gt; Access &gt; Other Accessibility Options &gt; Always display the keyboard selection cursor

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Access.html#idkeyname_1_575

##### Technical information
- **Friendly name of the setting:** Always display the keyboard selection cursor
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Adobe\Adobe Acrobat\DC\Access
- **Value Type:** REG_DWORD
- **Value Name:** bShowKeyboardSelectionCursor
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bLastAttachLinkMode
GUI mapping:
Edit &gt; Preferences &gt; Email Accounts &gt; Send file by email settings &gt; Always send files as a link (sign in required)

##### Technical information
- **Friendly name of the setting:** Always send files as a link (sign in required)
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Adobe\Adobe Acrobat\DC\UnifiedShare
- **Value Type:** REG_DWORD
- **Value Name:** bLastAttachLinkMode
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bAutoFill
Locks the auto-fill functionality on or off and disables the corresponding user interface item.  

Possible values:
- Enabled: Enable and lock auto-fill. 
- Disabled: Disable and lock auto-fill. 
 
GUI mapping: 
Preferences &gt; Forms &gt; Auto Complete drop down list.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FormPrefs.html#idkeyname_1_14080

##### Technical information
- **Friendly name of the setting:** Auto Complete
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bAutoFill
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bRuntimeHighlight
Specifies whether to highlight fields during data entry.

Possible values:
- Enabled: Shows a border on field hover.
- Disabled: Disables field border hover color.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FormPrefs.html#idkeyname_1_14248

##### Technical information
- **Friendly name of the setting:** Show border hover color for fields
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Adobe\Adobe Acrobat\DC\FormsPrefs\cRuntimeBGIdleColor
- **Value Type:** REG_DWORD
- **Value Name:** bRuntimeHighlight
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bBoxConnectorEnabled
Overrides "Disable cloud storage connectors" policy. Only supported on the Continuous track.

Possible values:
- Enabled: Enable connection to Box.
- Disabled: Disable connection to Box.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9966

##### Technical information
- **Friendly name of the setting:** Enable connection to the Box cloud
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bBoxConnectorEnabled
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bDisablePDFHandlerSwitching
Disables the ability to change the specified default handler (PDF viewer). 

When Reader and Acrobat are installed on the same machine or earlier versions of Acrobat already exist, you can choose which viewer is the default for PDF files. While Acrobat is the more capable, feature rich application, Reader X has a built in Protected Mode which is more secure (For security details, see the Application Security Guide).

This feature is a Adobe PDF handler-only feature: It does not enable switching to and from non-Adobe products and may or may not change the handling of other Acrobat supported formats; for example, it changes FDF and XDP, but not XFA or PDX.

Administrators interested in security may want to make Reader the default PDF viewer. Version X products will be able to switch between any product type and version back to 9.x.

For more information, see the PDF Ownership knowledge base article: https://kb2.adobe.com/cps/874/cpsid_87424.html

Note that UI configuration does not set any key in HKCU. Instead, changing the setting via the UI invokes the installer which sets the key in HKLM. The default application behavior varies depending on what is installed. A value of 1 disables the user's ability to change the default handler. 

Possible values:
- Enabled: Don't allow the user to change the default viewer.
- Disabled: Allow the user to change the default viewer.

GUI mapping:
Edit &gt; Preferences &gt; General &gt; Select Default PDF Handler

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_12191

##### Technical information
- **Friendly name of the setting:** Disable PDF handler switching
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bDisablePDFHandlerSwitching
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bDisableSharePointFeatures
Controls the application's ability to detect that a file came from a Sharepoint server, disables the check-out prompt, and removes the SharePoint specific menu items.

Possible values: 
- Enabled: Disable SharePoint and Office 365 integration. 
- Disabled: Don't disable SharePoint and Office 365 integration.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Workflows.html#idkeyname_1_32085

##### Technical information
- **Friendly name of the setting:** Disable the SharePoint and Office 365 integration features
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cSharePoint
- **Value Type:** REG_DWORD
- **Value Name:** bDisableSharePointFeatures
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bDisplayAboutDialog
Specifies whether or not to display the startup splash screen at every launch.

Possible values: 
- Enabled: Display the startup splash screen at every launch.
- Disabled: Don't display the startup splash screen. 

GUI mapping:
Splash screen

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Originals.html#idkeyname_1_16914

##### Technical information
- **Friendly name of the setting:** Display splash screen at launch
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Adobe\Adobe Acrobat\DC\Originals
- **Value Type:** REG_DWORD
- **Value Name:** bDisplayAboutDialog
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bDropboxConnectorEnabled
Overrides "Disable cloud storage connectors" policy. Only supported on the Continuous track.

Possible values:
- Enabled: Enable connection to Dropbox.
- Disabled: Disable connection to Dropbox.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_10016

##### Technical information
- **Friendly name of the setting:** Enable connection to the Dropbox cloud
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bDropboxConnectorEnabled
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bEnableAV2Enterprise
The new app UI is rolling out in phases over 2023. As of June, 25% of users will see the updated user interface.

Possible values:
- Enabled: Show the Modern Viewer.
- Disabled: Don't show the Modern Viewer.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_8799
##### Technical information
- **Friendly name of the setting:** Enable Modern Viewer
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bEnableAV2Enterprise
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bGoogleDriveConnectorEnabled
Overrides "Disable cloud storage connectors" policy. Only supported on the Continuous track.

Possible values:
- Enabled: Enable connection to Google Drive.
- Disabled: Disable connection to Google Drive.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_10116

##### Technical information
- **Friendly name of the setting:** Enable connection to the Google Drive cloud
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bGoogleDriveConnectorEnabled
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bOneDriveConnectorEnabled
Overrides "Disable cloud storage connectors" policy. Only supported on the Continuous track.

Possible values:
- Enabled: Enable connection to OneDrive.
- Disabled: Disable connection to OneDrive.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_10066

##### Technical information
- **Friendly name of the setting:** Enable connection to the OneDrive cloud
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bOneDriveConnectorEnabled
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bShowMsgAtLaunch
Specifies whether to show messages from Adobe when the product launches.  

Possible values:
- Enabled: Show messages from Adobe when the product launches.
- Disabled: Don't show messages from Adobe when the product launches.
 
GUI mapping:
Preferences &gt; General &gt; Show me messages when I launch Acrobat.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/IPM.html#idkeyname_1_15543

##### Technical information
- **Friendly name of the setting:** Show messages when I launch Acrobat
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cIPM
- **Value Type:** REG_DWORD
- **Value Name:** bShowMsgAtLaunch
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bSuppressSignOut
This policy setting provides you possibility to either disable or enable sign-in and sign-out Help menu item.

Possible values: 
- Enabled: Disable the Help menu item. 
- Disabled: Don't disable the menu item.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_10403

##### Technical information
- **Friendly name of the setting:** Sign-in and sign-out Help menu item
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bSuppressSignOut
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleAdobeDocumentServices
This setting does not affect Adobe Send for Signature (Acrobat Sign), preference synchronization, or third party connectors. For the base release, it also did not disable Send and Track (Share); however, it does control Send and Track with the July, 2015 release. For Acrobat Reader, this preference removes Create PDF, Export PDF, Organize, and Combine even if the ID has a subscription to those services. 

Possible values: 
- Enabled: Disable Document Cloud services.
- Disabled: Enable Document Cloud services.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9204

##### Technical information
- **Friendly name of the setting:** Disable Document Cloud service access
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bToggleAdobeDocumentServices
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleAdobeSign
Note that the Oct. 2018 Continuous track release renames "Send for Signature" as "Acrobat Sign". Continuous track installs should also set "Hide Signature tab" -policy . Preference behavior has not changed, but the UI to which it applies varies across product versions.

Possible values: 
- Enabled: Disable Adobe Send for Signature (Acrobat Sign).
- Disabled: Enable Adobe Send for Signature (Acrobat Sign).

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9392

##### Technical information
- **Friendly name of the setting:** Disable Adobe Send for Signature (Acrobat Sign)
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bToggleAdobeSign
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleFTE
Disables First Time Experience (FTE, Welcome tour/page) feature.

The first time experience (FTE) feature displays help content and tips when the application starts and also controls access to the Welcome Tour and Welcome page.

Possible values: 
- Enabled: Disable FTE features. 
- Disabled: Enable FTE features.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_10559

##### Technical information
- **Friendly name of the setting:** Disable FTE, Welcome tour/page feature
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bToggleFTE
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleManageSign
Specifies whether to remove the Signature tab from the Home page's left-hand pane, notifications, and sign tracking cards.
When set to 'Enabled' the signature tab is hidden, the user will not see any agreements received or sent for signature, and all Acrobat Sign notifications are disabled on the desktop. It also removes signature-related cards under the To Do list.

Possible values: 
- Enabled: Hide the Signature tab.
- Disabled: Show the Signature tab.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9348

##### Technical information
- **Friendly name of the setting:** Hide Signature tab
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bToggleManageSign
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleNotifications
When Disabled, feature-specific notifications are managed via the related service preference. When Enabled, this preference disables all notifications irrespective of the values of all other keys.

Possible values: 
- Enabled: Disable all desktop notifications.
- Disabled: Enable desktop notifications.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9698

##### Technical information
- **Friendly name of the setting:** Disable all in-product and desktop notifications
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bToggleNotifications
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bTogglePrefsSync
This preference disables and locks a new feature which synchronizes desktop preferences across devices on which the user is signed in with an Adobe ID. For more details about what preferences sync, see the Admin Guide: https://www.adobe.com/devnet-docs/acrobatetk/tools/AdminGuide/planning.html#preferences-synchronization

Possible values: 
- Enabled: Disable preferences synchronization. 
- Disabled: Enable preferences synchronization.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9582

##### Technical information
- **Friendly name of the setting:** Disable preferences synchronization
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bTogglePrefsSync
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleSendACopy
Specifies whether to hide the "Send a Copy" button from the Fill and Sign tool in Acrobat and Reader.

Possible values: 
- Enabled: Show the button.
- Disabled: Hide the button.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9255

##### Technical information
- **Friendly name of the setting:** Show "Send a Copy" button from the Fill and Sign tool in Acrobat and Reader
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bToggleSendACopy
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleShareFeedback
Specifies whether to show the Send Feedback icon.

By default, the UI displays a feedback icon so that users can easily send feedback to Adobe with one click.

Possible values: 
- Enabled: Show the icon.
- Disabled: Hide the icon.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_10671

##### Technical information
- **Friendly name of the setting:** Show the "Send Feedback" icon
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bToggleShareFeedback
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bToggleWebConnectors
Only supported on the Continuous track. Allows controlling in-product access to third party services for file storage. Dropbox support began with the Oct. 13, 2015 release. May 9, 2016: The preference now controls all the third-party connectors, including Box, OneDrive, and Dropbox (not SharePoint).

Possible values:
- Enabled: Disable 3rd party connectors.
- Disabled: Enable 3rd party connectors.

This preference disables 3rd party web connectors and their entry points from the product's UI, including in the Home view's left hand pane and under Add Account as well as custom Open/Save dialogs. If Document Cloud is also disabled, Open and Save dialogs revert to platform dialogs.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_9921

##### Technical information
- **Friendly name of the setting:** Disable cloud storage connectors
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown\cServices
- **Value Type:** REG_DWORD
- **Value Name:** bToggleWebConnectors
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bWhatsNewExp
This policy setting provides you possibility to either disable or enable What's New experience.

This feature was phased in incrementally over 2022. When enabled, the default user on first launch will see a What's New screen as well as a See new features notication. These UI items appear once.

Possible values: 
- Enabled: What's New experience is disabled. 
- Disabled: What's New experience is enabled.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/FeatureLockDown.html#idkeyname_1_8750

##### Technical information
- **Friendly name of the setting:** Disable What's New experience
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bWhatsNewExp
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bEnableJS
Toggles JavaScript execution on and off globally; when off, the PDF cannot execute JavaScript.

When the user's ability to create privileged locations is not disabled and locked, end users can bypass disabled JS by choosing Trust once or Trust Always via the Options button on the Yellow Message Bar. Admins can disable and lock JS execution by setting bDisableJavaScript to 0 in HKLM.

Possible values:
- Enabled: Acrobat JavaScript is enabled.
- Disabled: Acrobat JavaScript is disabled.

GUI mapping: 
Preferences &gt; JavaScript &gt; JavaScript panel &gt; Enable Acrobat JavaScript

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/JSPrefs.html#idkeyname_1_15664

##### Technical information
- **Friendly name of the setting:** Enable Acrobat JavaScript
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Adobe\Adobe Acrobat\DC\JSPrefs
- **Value Type:** REG_DWORD
- **Value Name:** bEnableJS
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bMIPCheckPolicyOnDocSave
More information: 
https://helpx.adobe.com/enterprise/kb/mpip-support-acrobat.html

Possible values:
- Enabled: Default and Mandatory labelling in Acrobat is enabled.
- Disabled: Default and Mandatory labelling in Acrobat is disabled.

##### Technical information
- **Friendly name of the setting:** MPIP: Enable Default and Mandatory labelling in Acrobat
- **Registry Hive:** HKEY_lOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bMIPCheckPolicyOnDocSave
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bMIPLabelling
More information:
https://helpx.adobe.com/enterprise/kb/mpip-support-acrobat.html

Possible values:
- Enabled: MPIP support enabled.
- Disabled: MPIP support disabled.

##### Technical information
- **Friendly name of the setting:** Enable MPIP support
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bMIPLabelling
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bAskBeforeInstalling
Specifies whether trust anchors should be imported silently or Acrobat should ask permission from the user.

Possible values: 
- Enabled: Enable and Install silently.
- Disabled: Enable and Ask before installing.

GUI mapping: 
Preferences &gt; Security &gt; Security Settings panel &gt; Ask before installing checkbox

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Security.html#idkeyname_1_18903

##### Technical information
- **Friendly name of the setting:** Ask before installing checkbox
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Adobe\Adobe Acrobat\DC\Security\cDigSig\cAdobeDownload
- **Value Type:** REG_DWORD
- **Value Name:** bAskBeforeInstalling
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bEnableCertificateBasedTrust
This lockable counterpart to "Automatically trust documents with valid certification" policy setting allows certified documents to bypass all the security restrictions that may be bypassed by other privileged locations. The exception is that this level of trust does not apply when the PDF is viewed in Protected View.

Possible values: 
- Enabled: Do make certified documents equivalent to privileged locations (trusted).
- Disabled: Don't make certified documents equivalent to privileged locations.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/TrustManager.html#idkeyname_1_29196

##### Technical information
- **Friendly name of the setting:** Allow certified documents to bypass all the security restrictions that may be bypassed by other privileged locations
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bEnableCertificateBasedTrust
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bEnhancedSecurityInBrowser
Toggles enhanced security when the application is running in the browser.

Possible values: 
- Enabled: Enable enhanced security in the browser.
- Disabled: Disable enhanced security in the browser.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/TrustManager.html#idkeyname_1_27749

##### Technical information
- **Friendly name of the setting:** Enhanced Security: Browser Mode
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bEnhancedSecurityInBrowser
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bEnhancedSecurityStandalone
Toggles enhanced security for the standalone application.

Possible values: 
- Enabled: Enable enhanced security in the standalone application.
- Disabled: Disable enhanced security in the standalone application.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/TrustManager.html#idkeyname_1_27798

##### Technical information
- **Friendly name of the setting:** Enhanced Security: Standalone Mode
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bEnhancedSecurityStandalone
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bProtectedMode
Protected Mode should be enabled to protect user systems and data.

Possible values: 
- Enabled: Do enable protected mode. 
- Disabled: Don't enable protected mode.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Privileged.html#idkeyname_1_17971

##### Technical information
- **Friendly name of the setting:** Enable Protected Mode at startup
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bProtectedMode
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bTrustCertifiedDocuments
This setting allows certified documents to bypass all the security restrictions that may be bypassed by other privileged locations. The exception is that this level of trust does not apply when the PDF is viewed in Protected View. To lock this setting, set "Allow certified documents to bypass all the security restrictions that may be bypassed by other privileged locations".

Possible values:
- Enabled: Do make certified documents equivalent to privileged locations (trusted).
- Disabled: Don't make certified documents equivalent to privileged locations.

GUI mapping:
Edit &gt; Preferences &gt; Security (Enhanced) &gt; Automatically trust documents with valid certification

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/TrustManager.html#idkeyname_1_29152

##### Technical information
- **Friendly name of the setting:** Automatically trust documents with valid certification
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Adobe\Adobe Acrobat\DC\TrustManager
- **Value Type:** REG_DWORD
- **Value Name:** bTrustCertifiedDocuments
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bTrustOSTrustedSites
Elevates locations that Internet Explorer trusts to privileged locations so that they may bypass security restrictions.

Prior to 10.1.1 and 9.4.7, trust was granted to Trusted Sites. With 10.1.2 and 9.5 and later, trust also includes Local Intranet zones. This setting essentially makes IE trust operate as if they were privileged locations. The feature can be disabled with bDisableOSTrustedSites.

Possible values:
- Enabled: Do automatically trust Windows OS zones.
- Disabled: Don't automatically trust Windows OS zones.

GUI mapping:
Edit &gt; Preferences &gt; Security (Enhanced) &gt; Automatically trust sites for my Win OS security zones

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/TrustManager.html#idkeyname_1_27955

##### Technical information
- **Friendly name of the setting:** Automatically trust sites for Win OS security zones
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Adobe\Adobe Acrobat\DC\TrustManager
- **Value Type:** REG_DWORD
- **Value Name:** bTrustOSTrustedSites
- **Enabled Value:** 1
- **Disabled Value:** 0

#### iProtectedView
Specifies whether to use Protected View never (default), for files from an untrusted location (recommended), or always.
			
The PV preferences were implemented in Acrobat 10.1 and are supported in Reader with 11.0. 
Possible values include, when enabling the policy:
- (default) Disable Protected View.
- (recommended) Enable Protected View for unsafe locations only
- Enable Protected View for all files.

Note that the Customization Wizard 11 created the preference in an incorrect location at HKLM\SOFTWARE\Policies\Adobe\(product name)\(version)\TrustManager. This bug is fixed in the Wizard DC.

GUI Mapping: 
Preferences &gt; Security (Enhanced) &gt; Protected View radio buttons.

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/TrustManager.html#idkeyname_1_29091

##### Technical information
- **Friendly name of the setting:** Protected View
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** iProtectedView
- **Enabled Values:**
    - **Disable Protected View:** 0
    - **Enable Protected View for all files:** 2
    - **Enable Protected View for unsafe locations:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### bAllowOpenFile
Specifies whether to open non-PDF attachments in their native application.

Possible values:
- Enabled: Allow opening of non-PDF file attachments with external applications.
- Disabled: Deny opening of non-PDF file attachments with external applications.

GUI mapping:
Edit &gt; Preferences &gt; Trust Manager &gt; Attachment panel &gt; Allow opening of Non-PDF file attachments with external applications

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Originals.html#idkeyname_1_17848

##### Technical information
- **Friendly name of the setting:** Allow opening of non-PDF file attachments with external applications
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Adobe\Adobe Acrobat\DC\Originals
- **Value Type:** REG_DWORD
- **Value Name:** bAllowOpenFile
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bLoadSettingsFromURL
Specifies whether or not trust anchors should be periodically downloaded from Adobe.

Possible values:
- Enabled: Do load settings from an URL.
- Disabled: Don't load settings from an URL.

GUI mapping:
Preferences &gt; Security &gt; Security Settings panel &gt; Load security settings from a server

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Security.html#idkeyname_1_21258

##### Technical information
- **Friendly name of the setting:** Load security settings from a server
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** Software\Adobe\Adobe Acrobat\DC\Security\cDigSig\cAdobeDownload
- **Value Type:** REG_DWORD
- **Value Name:** bLoadSettingsFromURL
- **Enabled Value:** 1
- **Disabled Value:** 0

#### bUpdater
Enable both updates to the product's web-plugin components as well as all services.		

Possible values:
- Enabled: Enables automatic updates. Users cannot disable those.
- Disabled: Disable automatic updates. It also removes update feature from "Help" &gt; "Check for Updates..." and disables the user interface items from "Preferences" &gt; "Updater and Help" &gt; "Check for updates".

More information:
https://www.adobe.com/devnet-docs/acrobatetk/tools/PrefRef/Windows/Updater-Win.html#idkeyname_1_29757

##### Technical information
- **Friendly name of the setting:** Enable automatic updates
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\Adobe Acrobat\DC\FeatureLockdown
- **Value Type:** REG_DWORD
- **Value Name:** bUpdater
- **Enabled Value:** 1
- **Disabled Value:** 0

#### EnableExternalBrowserAuth
If you want to enable it, select "Enable" and put value 1 to the value box.

##### Technical information
- **Friendly name of the setting:** Enable External Browser Authentication
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\NGL\Config
- **Value Type:** REG_SZ
- **Value Name:** EnableExternalBrowserAuth
- **Enabled Value:** 1
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### login_domain
Specify login domain, that will be use, when signing into Adobe-products e.g. Adobe Acrobat DC.

Example value:
example.com

##### Technical information
- **Friendly name of the setting:** Login Domain
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\Policies\Adobe\NGL\AuthInfo
- **Value Type:** REG_SZ
- **Value Name:** login_domain
- **Enabled Value:** example.com
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.