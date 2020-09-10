---
title: Description of Desktop Setup Tool logging errors
description: Describes errors that you may experience when you use Microsoft 365 Desktop Setup to install Microsoft 365 updates. Describes underlying conditions that trigger these errors.
author: simonxjx
ms.author: v-six
manager: dcscontentpm
audience: ITPro
ms.topic: troubleshooting
ms.service: o365-administration
localization_priority: Normal
ms.custom: 
  - CSSTroubleshoot
ms.reviewer: dahans, jhayes
appliesto:
- Microsoft 365
search.appverid: MET150
---
# Description of Microsoft 365 Desktop Setup Tool logging errors

_Original KB number:_ &nbsp; 2404500

When you try to install updates to client computers by using the Microsoft 365 Desktop Setup Tool, you may encounter errors. When an error occurs, an error message is recorded in the Microsoft 365 Desktop Setup Tool log file. This article describes the error messages that you might receive and the conditions that trigger these errors.

## More information

The Microsoft 365 Desktop Setup Tool log files can be found in the following locations:

- While the Microsoft 365 Desktop Setup Tool is running, you can press Ctrl+Shift+L to package the log files and save them to a location of your choice.
- On a computer that's running Windows 8.1, Windows 8, Windows 7, or Windows Vista, the log file can be found in one of the following locations:
  - C:\Users\<User_Name>\AppData\Local\Microsoft\Office365\DesktopSetup
  - %LOCALAPPDATA%\Microsoft\Office365\DesktopSetup

To further troubleshoot issues such as updates that couldn't be installed, view the following log files:

- The Application log
- The log files in the Windows Update log folder

When the installation of a required update isn't successful, the failure is logged in the Application log. Events that are related to the Microsoft 365 Desktop Setup Tool contain the following text:

By default, this information is also logged in the Windows Update log. The location of the Windows Update log file is %windir%\WindowsUpdate.log. The Windows Update log file might contain information about why a specific update wasn't installed.

The Microsoft 365 Desktop Setup Tool may also return MSI-specific errors and error codes as a result of the updates that are applied. These aren't errors that are generated by the Microsoft 365 Desktop Setup Tool. These are errors that are generated by the updates. To view the complete list of errors, see [MsiExec.exe and InstMsi.exe Error Messages](/previous-versions//aa368542(v=vs.85)).

### Microsoft 365 Desktop Setup errors

The following table describes the conditions that may trigger a Microsoft 365 Desktop Setup Tool error. The table also describes the error message that's received and that is recorded in the log.

|ID|Content|Description|
|---|---|---|
|AbortMessageDescription|Cancelling the installation may prevent you from connecting to Microsoft 365.|Description for the Abort dialog box|
|AbortMessageTitle|Do you want to cancel the installation?|Title text for the Abort dialog box|
|AdminMustSignInForUpdates|Your computer account does not have the permissions necessary to update your computer. Contact your system administrator to update your computer, and then run Microsoft 365 desktop setup again. If the problem persists, contact your system administrator.|Warning text when a regular user on Windows XP cannot install updates|
|AppConfigurationsAvailable|You can configure your desktop applications for use with Microsoft 365.|Tells the user that application configurations can be performed without administrator rights|
|CannotDownloadUpdatesDescription|Microsoft 365 desktop setup was unable to download updates to your computer. Verify your network connection and proxy settings, and then run Microsoft 365 desktop setup again. If the problem persists, contact your system administrator.|Text in the requirements screen about not being able to download updates|
|CannotDownloadUpdatesTitle|Microsoft 365 desktop setup was unable to download updates to your computer.|Title for requirements screen about not being able to download updates|
|ConfigurationDataNotAvailableFormatString|Configuration data for {0} is not available at this time.|{0} is the product name.|
|ConfigurationOptionsChanged|Your configuration options have changed. Verify your selections and select **Continue**.|Description that is below the header|
|ConfigureAppForMigrationIncompatibleDescription|Your version of {0} is not compatible with Microsoft 365. It will continue to work with your current settings, but will not work after you have been transitioned to Microsoft 365.|Right-side panel text|
|ConfigureLyncDisabledDescription|A compatible version of Microsoft Lync was not found.|Status pane text|
|ConfigureLyncDisabledTitle|Unable to configure Microsoft Lync|Status pane text|
|ConfigureLyncUncheckedDescription|You have chosen not to configure Microsoft Lync for use with Microsoft 365.|Status pane text|
|ConfigureLyncUncheckedTitle|Microsoft Lync will not be configured|Status pane text|
|ConfigureLyncUnprovisionedDescription|Your account has not been provisioned for the Lync service. Contact your administrator.|Status pane text|
|ConfigureLyncUnprovisionedTitle|Lync cannot be configured|Status pane text|
|ConfigureOutlookDisabledDescription|A compatible version of Microsoft Outlook was not found.|Status pane text|
|ConfigureOutlookDisabledTitle|Unable to configure Microsoft Outlook|Status pane text|
|ConfigureOutlookTransitionNotReadyDescription|Your Office account is being transitioned to Microsoft 365. However, your system administrator may not have completed the transition process. Verify with your system administrator that the transition process for your Microsoft 365 account has been completed before you configure Microsoft Outlook.|Right panel description for Outlook configuration for a user who is in transition but who is not ready for Microsoft 365 configuration|
|ConfigureOutlookUncheckedDescription|You have chosen not to configure Microsoft Outlook for use with Microsoft 365. You may not be able to receive email without Outlook Web Access.|Status pane text|
|ConfigureOutlookUncheckedTitle|Microsoft Outlook will not be configured|Status pane text|
|ConfigureOutlookUnprovisionedDescription|Your account has not been provisioned for use with Microsoft 365 Exchange servers. Contact your administrator.|Status pane text|
|ConfigureOutlookUnprovisionedTitle|Microsoft Outlook will not be configured|Status pane text|
|ConfigureSharePointNoActionTitle|Microsoft SharePoint will not be configured|Status pane text|
|ConfigureSharePointUnprovisionedDescription|Your account has not been provisioned with Microsoft SharePoint for Microsoft 365. Contact your administrator.|Status pane text|
|ConfigureSharePointUnprovisionedTitle|Microsoft SharePoint will not be configured|Status pane text|
|DeclineEulaMessageDescription|Declining the EULA will close Microsoft 365 without installing the required updates.|Description for the Decline EULA message box|
|ErrorAnotherInstallationInProgressTitle|Another installation is already running on this computer||
|ErrorAnotherVersionInstalledDescription|Before installation can continue, you must remove the existing version of this product.||
|ErrorAnotherVersionInstalledTitle|Another version of this product is already installed on this computer||
|ErrorBelowRequirementsTitle|Your computer does not meet the minimum system requirements|Title of minimum requirements dialog box|
|ErrorCodeFormatString|Error code:{0}|{0} is the error code number|
|ErrorConfigurationFailedDescription|This desktop application could not be configured. To complete the configuration, close any open applications and run this tool again. If the problem persists, contact your administrator for support.|Information pane description for a configuration update that fails|
|ErrorConfigurationFailedTitle|Configuration failed|Information pane title for a configuration update that fails|
|ErrorFailedToCreateShortcutsDescription|A Start menu shortcut for Microsoft 365 could not be created at this time. You can access the service by going to the Microsoft 365 home page.||
|ErrorFailedToCreateShortcutsTitle|Couldn't create Start menu shortcut||
|ErrorIncompatibleLanguageDescription|Contact Microsoft 365 Support for help.||
|ErrorIncompatibleLanguageTitle|This update is not available for your preferred location or language||
|ErrorInstallationWasCanceledDescription|Contact Microsoft 365 Support for help.||
|ErrorInstallationWasCanceledTitle|The installation was canceled||
|ErrorInstallFailedWithAnUncategorizedExitCodeDescription|Run the installation again. If the issue persists, contact Microsoft 365 Support.||
|ErrorInstallFailedWithAnUncategorizedExitCodeTitle|This update could not be installed on your computer||
|ErrorInstallFolderInaccessibleDescription|Restart your computer and try the installation again. If the issue persists, contact Microsoft 365 Support.||
|ErrorInstallFolderInaccessibleTitle|The installation folder is full or inaccessible||
|ErrorInsufficientDiskSpaceDescriptionFormatString|Required disk space: {0} MB<br/><br/>Available disk space: {1} MB<br/><br/><br/><br/>Free up disk space on your computer, and then select **OK** to continue.|Details related to insufficient space warning. {0} and {1} are integer values that show disk space.|
|ErrorInsufficientDiskSpaceTitle|Your computer does not have enough disk space|Title for insufficient disk space warning message|
|ErrorMicrosoftUpdateNotAddedDescription|One or more required updates cannot be installed. To install these updates, try again, or contact your system administrator.||
|ErrorMicrosoftUpdateNotAddedTitle|Cannot access a required update||
|ErrorMissingUserConfigurationInfoDescription|All of the required information for the update could not be downloaded, so the update wasn't installed.||
|ErrorMissingUserConfigurationInfoTitle|Update was not installed||
|ErrorNoInternetConnectionDescription|Check your Internet connection and run the installation again.||
|ErrorNoInternetConnectionTitle|Microsoft 365 cannot detect your Internet connection.||
|ErrorNoneDescription||Intentionally blank|
|ErrorNoneTitle||Intentionally blank|
|ErrorNotCompatibleWithOSDescription|If the issue persists, contact Microsoft 365 Support.||
|ErrorNotCompatibleWithOSTitle|This update is not compatible with your version of Windows||
|ErrorNotCompatibleWithWindowsInstallerDescription|The update can be obtained from Windows Update.||
|ErrorNotCompatibleWithWindowsInstallerTitle|Your computer requires an update from the Windows Installer Service||
|ErrorNotEnoughDiskSpaceDescription|Create more space on your computer, and then run the installation again.||
|ErrorNotEnoughDiskSpaceTitle|Your computer does not have enough free space||
|ErrorOpeningLinkDescriptionFormatString|There was a problem opening the web page {0} in your default browser. Check the settings of your default browser and try again.|Message box description. {0} is the URL that failed to open.|
|ErrorOpeningLinkTitle|Unable to open your default browser|Message box title|
|ErrorOptInMuDescription|Your system policy does not allow you to connect to the Microsoft Update services, which will prevent some updates from being installed. Ensure that you have permission to connect to the Microsoft Update services or contact your system administrator for additional assistance.||
|ErrorOptInMuTitle|Your computer is not allowed to connect to the Microsoft Update service||
|ErrorRebootRequiredDescription|To complete the installation, restart your computer.||
|ErrorRebootRequiredTitle|You must restart your computer||
|ErrorRemoteInstallationFailedDescription|Sign in to the remote computer and run the installation manually.||
|ErrorRemoteInstallationFailedTitle|The remote installation failed||
|ErrorSkippedDueToEulaNotAcceptedDescription|The terms of the service agreement for this update were not accepted.||
|ErrorSkippedDueToEulaNotAcceptedTitle|The update was not installed||
|ErrorSkippedDueToPrereqFailureDescription|A prior update failed to install, which is preventing this update from installing. Run the installation again. If the issue persists, contact your system administrator.||
|ErrorSkippedDueToPrereqFailureTitle|This update could not be installed||
|ErrorUnknownDescription|Run the installation again. If the issue persists, contact Microsoft 365 Support.||
|ErrorUnknownTitle|This update could not be installed on your computer||
|ErrorUnsupportedSignInAssistantAlreadyInstalledDescription|Uninstall the Sign-In Assistant and try the installation again.||
|ErrorUnsupportedSignInAssistantAlreadyInstalledTitle|The version of Microsoft Online Services Sign-In Assistant that is already running on your computer is no longer supported||
|ErrorUpdateNotApprovedDescription|If the issue persists, contact your system administrator.||
|ErrorUpdateNotApprovedTitle|This update is not approved for your organization||
|ErrorUpdateUponRestart|Microsoft 365 will attempt to update your computer upon restart.||
|EulaDescription|Review the service agreements. To continue, select **I accept**.|Description of the EULA screen|
|EulaLink|View the Microsoft 365 privacy policy.|Text of the EULA link|
|EulaTitle|Review and accept the service agreements|Title of the EULA screen|
|FinishUpdatesFailedFormatString|Updates that failed to install: {0}|This string would be part of a final **update complete** report list. It is formatted accordingly.|
|LoggingSaveErrorDescription|Microsoft 365 desktop setup was unable to create your Microsoft 365 desktop setup log.|Description text for save error dialog box|
|LoggingSaveErrorTitle|Error creating Microsoft 365 desktop setup log|Title text for save error dialog box|
|MainDescriptionSomeUpdatesFailed|Some updates failed to install. Select a failed update for more information. Save your work and restart your computer. If you want to continue working, you can choose to restart later.|Description of some updates failed screen|
|MainLinkTroubleshoot|Learn how to troubleshoot installation errors||
|OfficeReleasesSupported|Your version of Microsoft Office is not compatible with Microsoft 365. Microsoft 365 only supports released versions of Office and Office service packs. Update your version of Office to a supported version, and then run Microsoft 365 again.|Text in prerequisites screen about supported Office releases|
|StatusConfigureFailed|Configuration failed|Status column value|
|StatusDownloadFailed|Download failed|Status column value|
|StatusInstallFailed|Installation failed|Status column value|
|UserConfigurationDownloadErrorDescription|The information required to configure your computer for Microsoft 365 could not be downloaded. If the issue persists, contact Microsoft 365 Support.|Description of error dialog box when user configuration data cannot be downloaded|
|UserConfigurationDownloadErrorTitle|Application configuration incomplete|Title of error dialog box when user configuration data cannot be downloaded|
|UserConfigurationVersionErrorDescription|Launch the latest version of the application from the Microsoft Online Services Portal.|Description of the error dialog box that states that user has to run the latest version of the application through the Information Worer (IW) Portal|
|UserConfigurationVersionErrorTitle|This version of the application is no longer supported.|Title of the error dialog box that states that the user has to run the latest version of the application through the W Portal|
|WarningBelowSystemRequirements|The version of Microsoft Windows or Microsoft Office you are using is not compatible with Microsoft 365.|Text for the system requirements dialog box|
|WarningCloseApplicationsToContinueTitle|You must close the following applications before Microsoft 365 can be configured:|Title of the **You need to close** dialog box. Description is a list of application names.|
||||

## References

For more information about issues that could occur when you run Microsoft 365 Desktop Setup, see [Microsoft 365 Desktop Setup Tool cannot download updates or you receive an "Your computer is not allowed to connect to the Microsoft Update service" error message](https://support.microsoft.com/help/2392274).

Still need help? Go to [Microsoft Community](https://answers.microsoft.com/).