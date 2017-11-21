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