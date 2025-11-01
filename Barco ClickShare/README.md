# Barco ClickShare

This repository includes custom Administrative Templates for Barco ClickShare that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template
Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Barco ClickShare | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/ClickShare/Policy/ClickShareAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```AutoUpdateEnable``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/AutoUpdateEnable``` | String | ```<enabled/> <data id="AutoUpdateEnable" value="true"/>```
| ```BetaProgramDisable``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/BetaProgramDisable``` | String | ```<enabled/>```
| ```CalendarIntegrationEnabledByAdmin``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/CalendarIntegrationEnabledByAdmin``` | String | ```<enabled/> <data id="CalendarIntegrationEnabledByAdmin" value="false"/>```
| ```ProductUsageAnalyticsDisable``` | (See below) | ```./Device/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/ProductUsageAnalyticsDisable``` | String | ```<enabled/>```
| ```CalendarIntegration``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/CalendarIntegration``` | String | ```<enabled/> <data id="CalendarIntegration" value="false"/>```
| ```PresentSensePromotionShown``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/PresentSensePromotionShown``` | String | ```<enabled/> <data id="PresentSensePromotionShown" value="false"/>```
| ```UltrasoundIntegration``` | (See below) | ```./User/Vendor/MSFT/Policy/Config/ClickShare~Policy~ClickShare/UltrasoundIntegration``` | String | ```<enabled/> <data id="UltrasoundIntegration" value="false"/>```

### Descriptions
More details of the settings can be found this chapter.

#### AutoUpdateEnable
To control if the app will be automatically updated or not.

Possible values:
- true: App will be automatically updated.
- false: App will not be automatically updated.

More information:
https://www.barco.com/en/support/knowledge-base/3329-what-are-the-available-parameters-for-the-clickshare-desktop-app-installer-msi

> [!NOTE]
> - If you want to disable automatic updates, please make sure that policy is enabled but the value must be set to ```"false"```

##### Technical information
- **Friendly name of the setting:** Enable automatic updates
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\WOW6432Node\Barco\ClickShare Installer
- **Value Type:** REG_SZ
- **Value Name:** AutoUpdateEnable
- **Enabled Value:** true
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### BetaProgramDisable
To control the “Beta Program” UI option.

Options:
- Enabled: No UI option for Beta Program in the app.
- Disabled: UI option for Beta Program visible in the app.

More information:
https://www.barco.com/en/support/knowledge-base/3329-what-are-the-available-parameters-for-the-clickshare-desktop-app-installer-msi

##### Technical information
- **Friendly name of the setting:** Disable Beta Program
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\WOW6432Node\Barco\ClickShare Installer
- **Value Type:** REG_DWORD
- **Value Name:** BetaProgramDisable
- **Enabled Value:** 1
- **Disabled Value:** 0

#### CalendarIntegrationEnabledByAdmin
To turn on and off "Calendar Integration" and its UI option by Admin.

Possible values:
- true: Calendar integration is enabled.
- false: Calendar integration is disabled.

More information:
https://www.barco.com/en/support/knowledge-base/3329-what-are-the-available-parameters-for-the-clickshare-desktop-app-installer-msi

> [!NOTE]
> - If you want to disable calendar integration, please make sure that policy is enabled but the value must be set to ```"false"```

##### Technical information
- **Friendly name of the setting:** Calendar integration enabled by Admin
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\WOW6432Node\Barco\ClickShare Installer
- **Value Type:** REG_SZ
- **Value Name:** CalendarIntegrationEnabledByAdmin
- **Enabled Value:** true
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### ProductUsageAnalyticsDisable
To turn on and off "Usage Statistics".

Options:
- Enabled: "Usage Statistics" is turned off.
- Disabled: "Usage Statistics" is turned on.

More information:
https://www.barco.com/en/support/knowledge-base/3329-what-are-the-available-parameters-for-the-clickshare-desktop-app-installer-msi

##### Technical information
- **Friendly name of the setting:** Disable Product Usage Analytics
- **Registry Hive:** HKEY_LOCAL_MACHINE
- **Registry Path:** SOFTWARE\WOW6432Node\Barco\ClickShare Installer
- **Value Type:** REG_DWORD
- **Value Name:** ProductUsageAnalyticsDisable
- **Enabled Value:** 1
- **Disabled Value:** 0

#### CalendarIntegration
To turn on and off "Calendar Integration"

Possible values:
- true: Calendar integration is enabled.
- false: Calendar integration is disabled.

More information:
https://www.barco.com/en/support/knowledge-base/3329-what-are-the-available-parameters-for-the-clickshare-desktop-app-installer-msi

> [!NOTE]
> - If you want to disable calendar integration, please make sure that policy is enabled but the value must be set to ```"false"```

##### Technical information
- **Friendly name of the setting:** Enable Calendar integration
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Barco\ClickShare Client
- **Value Type:** REG_SZ
- **Value Name:** CalendarIntegration
- **Enabled Value:** true
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### PresentSensePromotionShown
To show or hide present sense promotions.

Possible values:
- true: Present Sense Promotions are showing.
- false: Present Sense Promotions are hidden.

More information:
https://www.barco.com/en/support/knowledge-base/3329-what-are-the-available-parameters-for-the-clickshare-desktop-app-installer-msi

> [!NOTE]
> - If you want to hide sense promotions, please make sure that policy is enabled but the value must be set to ```"false"```

##### Technical information
- **Friendly name of the setting:** Show Present Sense Promotion
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Barco\ClickShare Client
- **Value Type:** REG_SZ
- **Value Name:** PresentSensePromotionShown
- **Enabled Value:** true
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### UltrasoundIntegration
To enable or disable Ultrasound Integration.

Possible values:
- true: Ultrasound Integration is enabled.
- false: Ultrasound Integration is disabled.

More information:
https://www.barco.com/en/support/knowledge-base/3329-what-are-the-available-parameters-for-the-clickshare-desktop-app-installer-msi

> [!NOTE]
> - If you want to disable ultrasound integration, please make sure that policy is enabled but the value must be set to ```"false"```

##### Technical information
- **Friendly name of the setting:** Enable Ultrasound Integration
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Barco\ClickShare Client
- **Value Type:** REG_SZ
- **Value Name:** UltrasoundIntegration
- **Enabled Value:** true
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.