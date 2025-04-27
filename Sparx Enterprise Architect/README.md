# Sparx Enterprise Architect

This repository includes custom Administrative Templates for Sparx Enterprise Architect that can be used on your on-prem environment or Microsoft Intune.

## OMA-URI of ADMX-template

> [!IMPORTANT]  
> Unfortunately you cannot set "AutoCheckoutEx" using this ADMX-template. Instead you need to use another methods. Some of these methods are listed below:
> - **On-Prem:** "Registry" section from Group Policy Management Editor.
> - **Cloud:**
>   - **Option 1:** [Remediations](https://learn.microsoft.com/en-us/intune/intune-service/fundamentals/remediations) -feature from Intune.
>   - **Option 2:** Deploy PowerShell-script, that will implement "AutoCheckoutEx" with needed value as an application and add AutoCheckoutEx" with needed value to detection method.
>   - **Option 3:** Wrap Sparx Enterprise Architect installer to [PSAppDeployToolkit](https://psappdeploytoolkit.com/). For post-installation section import "AutoCheckoutEx" with needed value. Remember to add "AutoCheckoutEx" and needed value to detection method when deploying Sparx Enterprise Architect as an application.

Here you can see OMA-URI information for released ADMX-template, that can be deployed via Intune using ingestion.

| ADMX-template | OMA-URI |
|---------------|---------|
| Sparx Enterprise Architect | ```./Device/Vendor/MSFT/Policy/ConfigOperations/ADMXInstall/SparxEnterpriseArchitect/Policy/SparxEnterpriseArchitectAdmx``` |

## OMA-URI of settings
Here you can see OMA-URI information of the settings that are part of this ADMX-template, that can be deployed via Intune using ingestion with ingested ADMX-template.

| Name | Description | OMA-URI | Data type |  Recommended Value
|---------|---------|---------|---------|---------|
| ```SKT``` | [See below](#SKT) | ```./User/Vendor/MSFT/Policy/Config/SparxEnterpriseArchitect~Policy~SparxEnterpriseArchitect/SKT``` | String | ```<enabled/>```
| ```JET4``` | [See below](#JET4) | ```./User/Vendor/MSFT/Policy/Config/SparxEnterpriseArchitect~Policy~SparxEnterpriseArchitect/JET4``` | String | ```<enabled/>```
| ```INIFILE_VERSION``` | [See below](#INIFILE_VERSION) | ```./User/Vendor/MSFT/Policy/Config/SparxEnterpriseArchitect~Policy~SparxEnterpriseArchitect/INIFILE_VERSION``` | String | ```<enabled/>```
| ```SSKSAddress``` | [See below](#SSKSAddress) | ```./User/Vendor/MSFT/Policy/Config/SparxEnterpriseArchitect~Policy~SparxEnterpriseArchitect/SSKSAddress``` | String | ```<enabled/> <data id="SSKSAddress" value="ssks://ssks.example.com:7770"/>```
| ```SSKSDisplayAddress``` | [See below](#SSKSDisplayAddress) | ```./User/Vendor/MSFT/Policy/Config/SparxEnterpriseArchitect~Policy~SparxEnterpriseArchitect/SSKSDisplayAddress``` | String | ```<enabled/> <data id="SSKSDisplayAddress" value="ssks://ssks.example.com:7770"/>```
| ```SSKSPassword``` | [See below](#SSKSPassword) | ```./User/Vendor/MSFT/Policy/Config/SparxEnterpriseArchitect~Policy~SparxEnterpriseArchitect/SSKSPassword``` | String | ```<enabled/> <data id="SSKSPassword" value=""/>```

### Descriptions
More details of the settings can be found this chapter.

#### SKT
If you are configuring zero config client support, you need to enable this setting for enabling SKT. Enabling this setting is required.

More information:
https://sparxsystems.com/enterprise_architect_user_guide/17.0/getting_started/zero_config_support.html

> [!NOTE]  
> If you want to disable the setting via Intune, please make sure that value is then set to ```<disabled/>```

##### Technical information
- **Friendly name of the setting:** Enable SKT for zero config client support
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Sparx Systems\EA64\EA\OPTIONS
- **Value Type:** REG_DWORD
- **Value Name:** SKT
- **Enabled Value:** 1
- **Disabled Value:** 0

#### JET4
If you are configuring zero config client support, you need to enable this setting for enabling JET4. Enabling this setting is required.

More information:
https://sparxsystems.com/enterprise_architect_user_guide/17.0/getting_started/zero_config_support.html

##### Technical information
- **Friendly name of the setting:** Enable JET4 for zero config client support
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Sparx Systems\EA64\EA\OPTIONS
- **Value Type:** REG_DWORD
- **Value Name:** JET4
- **Enabled Value:** 1
- **Disabled Value:** 0

#### INIFILE_VERSION
If you are configuring zero config client support, you need to enable this setting for enabling appropriate INIFILE_VERSION.

Hint:
Enable this setting (that is required) as this will apply following registry value below.
"INIFILE_VERSION"=dword:00000043

More information:
https://sparxsystems.com/enterprise_architect_user_guide/17.0/getting_started/zero_config_support.html

##### Technical information
- **Friendly name of the setting:** Enable appropriate INIFILE_VERSION value for zero config client support
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Sparx Systems\EA64\EA\OPTIONS
- **Value Type:** REG_DWORD
- **Value Name:** INIFILE_VERSION
- **Enabled Value:** 43
- **Disabled Value:** 0

#### SSKSAddress
If you are configuring zero config client support, you need to configure this setting. Enabling and configuring SSKSAddress is required.

Hint:
Configure same value, that you have configured to setting "Configure SSKSDisplayAddress for zero config client support".

More information:
https://sparxsystems.com/enterprise_architect_user_guide/17.0/getting_started/zero_config_support.html

##### Technical information
- **Friendly name of the setting:** Configure SSKSAddress for zero config client support
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Sparx Systems\EA64\EA\OPTIONS
- **Value Type:** REG_SZ
- **Value Name:** SSKSAddress
- **Enabled Value:** ssks://ssks.example.com:7770
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.

#### SSKSDisplayAddress
If you are configuring zero config client support, you need to configure this setting. Enabling and configuring SSKSDisplayAddress is required.

Hint:
Configure same value, that you have configured to setting "Configure SSKSAddress for zero config client support".

More information:
https://sparxsystems.com/enterprise_architect_user_guide/17.0/getting_started/zero_config_support.html

##### Technical information
- **Friendly name of the setting:** Configure SSKSAddress for zero config client support
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Sparx Systems\EA64\EA\OPTIONS
- **Value Type:** REG_SZ
- **Value Name:** SSKSDisplayAddress
- **Enabled Value:** ssks://ssks.example.com:7770
- **Disabled Value:** N/A

#### SSKSPassword
If you are configuring zero config client support, you need to configure this setting. Enabling this setting is required.

Hint:
Enable this setting and keep value empty.

More information:
https://sparxsystems.com/enterprise_architect_user_guide/17.0/getting_started/zero_config_support.html

##### Technical information
- **Friendly name of the setting:** Configure SSKSPassword for zero config client support
- **Registry Hive:** HKEY_CURRENT_USER
- **Registry Path:** SOFTWARE\Sparx Systems\EA64\EA\OPTIONS
- **Value Type:** REG_SZ
- **Value Name:** SSKSPassword
- **Enabled Value:** 
- **Disabled Value:** N/A

> [!NOTE]  
> N/A in this context means that registry key is not existed.
