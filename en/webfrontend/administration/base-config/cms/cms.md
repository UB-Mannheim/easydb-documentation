# CMS

Connecting CMS-Systems in easydb works via [Plugins](/webfrontend/datamanagement/features/plugins/plugins.html). The settings for the connection of CMS systems are made here.


## Wordpress {#wordpress}

![Configuration: Wordpress in easydb](bc_cms_wp.jpg)

|CMS|Field|Description|
|--|--|--|
|Wordpress|Instance name|It is possible to add one or more instances. You must assign a name for each instance.|
||URL| The Worldpress URL to which the export is supposed to be deliverd.|
||Authentication|Authentication type HTTP: <br> login name and password for Wordpress administration. |
|||Authentication type OAuth 1.0a: <br >Copy the client key and client secret of the (prepared) application user from Wordpress <br > Click "Generate Key" to connect to Wordpress, authenticate yourself and get a token or token secret. |



> NOTE: At least Wordpress 4.7, an active JSON-Rest-API (is default) and a configured authentication are required. For use in the frontend, the user or group needs the [system right](/webfrontend/rightsmanagement/rightsmanagement.html#acl_system) "Wordpress" and "Allow Wordpress Export".

Instructions for installing the plugin are [here](/sysadmin/konfiguration/plugin/plugin.html).

## Falcon.io {#falconio}

![Configuration: Falconio](falconio.jpg)

|CMS|Field|Description|
|--|--|--|
| Falcon.io | Instance name| You can create one or more instances here. You must assign a name for each instance. |
|| API_Key | For the use of the RESTful API the unique API Key from falcon.io is needed. |
|| Active | The checkbox can be used to activate and deactivate the API for for each instance.|

## TYPO3 {#typo3}

![Configuration: TYPO3-Plugin für easydb](bc_cms_typo3.jpg)

After the successful [plugin configuration](../../../sysadmin/konfiguration/plugin/plugin.html) in a [YAML file](../../../sysadmin/konfiguration/yaml/yaml.html) through a system administrator, you can make settings for the TYPO3 plugin here.

|CMS|Field|Description|
|--|--|--|
|TYPO3 (starting with Version 7)|Activate API|Activates the [Plugin](../../datamanagement/features/plugins/plugins.html). |
||Send files via browser| With the TYPO3 plugin, easydb can be used for exporting files. If the export from the easydb server to the Typo3 server is not directly possible, the option for export via browser can be activated.|
||Maximum file size| Limit for files, if they are sent via the browser. |
||Metadata mapping|Settings for the easydb export to Typo3.<br><br>**- Standard only -**: Without a mapping Standard A will be mapped to *title* and Standard B to *description*.<br><br> **Individual mapping**: Individuel Mappings can be created as described in [Metadaten mapping](../profiles/profiles.html). All mappings appear in the pulldown. |
