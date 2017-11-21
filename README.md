# MaxCode Patch Notes
If you notice any new or unexpected behavior not covered in these patch notes, please report it to <support@practicemax.com>
Please use the subject line to provide a brief description of the bug, error, or unexpected behavior. For instance, if the chart comments aren't saving correctly, your e-mail might have the subject line ```MaxCode - Chart Comments Error```

## Release History:
- [1.8.1 - *Update for eCW Integration*](#181---update-for-ecw-integration)
    - eCW Chart Creation
    - Credential Security Improvements
    - Automated coding of drug screens and confirmations
    - Encounter Sweep Auditing Bug
    - Dual Coding Reconciliation - Date Time Bug
    - User Admininistration Enhancements
- [1.8.0 - *Dual Coding Update*](#180---dual-coding-update)
    - Interface Changes
    - Security Groups
    - Encounter Sweeps
    - Dual Coding Workflow
    - Dual Coding and Training Workflow Management
    - Dual Coding Reconciliation
- [1.7.0 - *Multi-Specialty Update*](#170---multi-specialty-update)
    - Readability improvement for encounter documents - update to Coding and Exceptions screens
    - MaxNote - new MetaData Type
    - User Authentication and Account Security
- [1.6.0](#160)
    - Insurance Data Backfill
    - Search Screen Improvements
    - Sending Charts between Billing and Coding Support
    - System Agnostic Imports and Exports
- [1.5.0](#150)
    - Added Patch Notes
    - Search Screen View Switching
    - Alert for 'Date Notification Sent' field
    - Required Comment to Remove Document

## 1.8.1a.20171120 - *Update for eCW Integration*
### eCW Chart Creation (New Source System Integration)
- Allows seamless inegration with clients using eCW.
- Locked progress notes from eCW can now be imported into MaxCode.
- Imported documents are linked to an encounter as a chart file type.
### Credential Security Improvements (Login Screen)
- Date and time of last login and last password change are now being recorded.
- Accounts with no login activity in the last 30 days are automatically disabled.
- Passwords changes are enforced every 90 days.
### Automatic coding of drug screens and confirmations (Automated Workflow)
- Encounters specialized for drug testing can now be automatically coded.
- Automatic coding will not occur until insurance demographics have been mapped.
### Encounter Sweep Auditing Bug (Sweep Screen)
- Correct a failure to properly report the audit trail of encounters swept to Ready-for-Billing status.
### Dual Coding Reconciliation - Date Time Bug (Reconciliation Screen)
- A bug was corrected on the dual coding reconciliation screen where current time was recorded along with the date.
    - Fields effected were Date Onset, Admit Date, Discharge Date, and cpt DOS.
- Time differences will no longer cause some unnecessary reconciliations to escalate to Manager.
### User Admininistration Enhancements (User Administration Screen)
- Search screen now has filters for Active/Inactive accounts and a search by username.

## 1.8.0.20170830 - *Dual Coding Update*
### Interface Changes
- The login screen and menu bar adapted to smaller screens.
### Security Groups (New Screen and Changes to User Management Screen)
- Security groups have been implemented in user management process. Users receive their permissions by being assigned to 1 or more security groups. With these changes, a user can perform different coding roles for different practices.
- There is a security group management page to create and control permissions, add or remove users from groups, and show a users overall permissions with what groups they belong to.
- The user account page displays to a user their overall permissions.
### Encounter Sweeps (New Encounter Sweep Screen)
- In order to prevent a buildup of random-qc charts in the escalation workflow beyond what QC and management users can work, a screen has been created where certain managers will be able to mark charts as "ready-for-billing". Dual Coded charts are not available for sweeps.
### Dual Coding Workflow (Various Screens)
- The new dual coding process allows a single chart to be coded by two different coders. If there are differences between the dual coded charts, they are sent through a reconciliation process by QC.
### Dual Coding and Training Workflow Management (New Dual Coding Management Screen)
- Dual Coding and Training is controlled on a practice-by-practice or location-by-location basis.
- Dual Coding charts must be completed by two coders before being marked ready for billing; Training charts allow a coder to code a chart and receive feedback comparing their chart to the version that was marked "ready-for-billing".
### Dual Coding Reconciliation (New QC Reconciliation Screen)
- The Dual Coding Reconciliation screen allows certain QC users to compare both versions of a Dual Coded chart, then select one copy and mark it to be billed.
- This screen will highlight in red any differences between the two versions of the chart.
### Bug Fixes and Minor Changes
- "MRN" and "Patient Demographic - City" fields have been widened; Charts brought in to MaxCode with very long City names and MRNs will no cause errors.
- Minor enhancement to manual chart creation process to prevent certain errors when combining multiple pdfs.
- Minor enhancement to manual chart creation process to prevent errors related to case sensitivity in file names.
- On chart and exception screen, documents will now sort slightly more intuitively.
- Bugfix on the 'units' for potential codes: units will no longer reset to 1 after being set by the coder.

## 1.7.0.20170327 - *Multi-Specialty Update*
### Readability improvement for encounter documents - update to Coding and Exceptions screens
- The document name will now be visible when you mouse over the link to a source document. This is intended to help determine which chart document is most recent or which applies to a particular date of service
- Handling for additional medical specialties - new fields on Coding and Exceptions screens
- In order to facilitate coding for visits that take place over multiple days, we have added "Admit Date", "Discharge Date", "Accession Number" and charge-level "override DOS" to the chart and exception screens.
- There is a new "Refering Provider" field. It will allow you to select valid referring providers. If a referring provider is missing, please contact support@practicemax.com.
### MaxNote - new MetaData Type
- MaxNote is a new metadata type that will be used to assist in capturing practice or specialty specific data necessary for charge import after coding is completede. Managers will be adding necessary MaxNote metadata fields to the appropriate practices and briefing you on their use.
### User Authentication and Account Security
- ~~Within the coming days and on a continuing basis, users who have not viewed or coded a chart for at least 60 days will be de-activated.~~ If your account is de-activated in error please contact your manager.
- ~~Within the coming days and on a continuing basis, users will have to update their passwords at least every 90 days.~~ When it is time to renew your password, you will be able to login as usual, but will not be able to proceed to coding screens until you have designated a new password.
- Several other background changes have been made to user authentication to improve security and clarity.
### Bug Fixes and Minor Changes
- Sometimes, a chart would open in view only mode after exceptions on it had been resolved. These will now open in the correct mode.
- In Microsoft Edge, the search screen would sometimes fail to appropriately evaluate all filters selected. This has been corrected.
- In Microsoft Internet Explorer, some data was lost during the manual chart linking process. Support for Internet Explorer has been improved so that manual chart linking works correctly.

## 1.6.0.20161227
### Insurance Data Backfill (Demographics Screen - Insurance Tab - improved functionality)
- We've allowed insurance information from SequelMed to backfill into the appropriate fields in MaxCode in order to make it easier on users and reduce room for error. You will no longer need to manually copy or re-type the information retrieved. In order to use this feature, simply select the correctly mapped insurance from each dropdown, then click save.
### Search Screen Improvements (Chart Search Screen- improved functionality)
- Automatic retrieval of previous search: The chart search screen will now 'remember' your selections in the dual coding filter and the coder/support view selector. When you leave the search screen and return, a search will automatically initiate using your last search parameters and display the results in either the Coder View or Support View as they were when you left the page.
- Dropdown Filters and Select All buttons- Dropdowns on the search screen have been replaced with multi-select search boxes. Simply 'tab into' or click on one of the fields and you can begin typing to narrow down the list of options. You can click, use the space bar, or use the right arrow key to toggle an item in the dropdown; the left arrow key will always deselect the current item. There is also a new 'Select All' option in each dropdown that will select or deselect all currently available entries. Press enter to initiate a search from anywhere on the page. For instance, when looking for all charts that are missing an element, you could tab to or click on the 'Detailed Status' box, type "missing", then click on 'Select All'.
- In order to enable this change, dropdowns will no longer open on mouse-over.
### Sending Charts between Billing and Coding Support (Exceptions Screen - improved functionality)
- Billing Support users will now be able to send items requiring coding review to Coder Support users for review. This option has been added to the radio buttons near the Submit button.
- Coder Support users will now be able to send items requiring billing review to Billing Support users for review. This option has been added to the radio buttons near the Submit button.
### System Agnostic Imports and Exports (Back-end - improved functionality)
- Improvements have been made to allow MaxCode to work with additional Practice Management and Electronic Health Records Systems. As part of these changes, we've made handling of practices, locations, providers, and medical codes more robust; for the time being you should not notice any changes, but onboarding of new practices will be more flexible.
### Bug Fixes and Minor Changes
- Improved logging on updates to encounter documents
- Improved handling of "File Load: Chart Exceptions" and manual linking of chart documents.
- Fixed access to the Exceptions Screen for users in the Billing Support Role.

## 1.5.0.20160926
### Patch Notes (New Screen)
- MaxCode now has formal versioning and patch notes. Please login and click the 'Patch Notes' header (or navigate to maxcode.practicemax.com/patchnotes) to see a summary of changes made in each patch.
### Search Screen View Switching (Search Screen - new functionality)
- Users that are able to interact with both the coding screen and the exceptions screen will see a new dropdown that allows the search screen to switch between the exception and coding views at will.
### Alert for 'Date Notification Sent' field (Exception Screen - improved functionality)
- As we add automated notification to the system, we've also added an alert to the 'Date Notif Sent' field. If you put today's date into the field after 6PM MST of each day, then the system will let you know that no automated notification will be sent. If an automated notification must be sent, please go back and enter tomorrow's date.
### Required Comment to Remove Document (Exception Screen - improved security)
- In order to remove a file (such as a duplicated chart image) from an encounter, a chart comment is now required.
### Bug Fixes and Minor Changes
- Fixed several instances of dropdowns not sorting alphabetically.
- Added additional validation to the export of demographics into the billing system
- Improvement to the database records so that as new physician chart documents come in for a chart, the documents are included in the Chart History Table.