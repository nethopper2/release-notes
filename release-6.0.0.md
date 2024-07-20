# Release Notes - KAOPS 6.0.0 Beta 8

## Release Code Name - "Jade"

## Release Date 2024-07-19

# New features
- MFA
- GitHub and Google SSO supported
- Okta support
- ArgoCD Sync Wave, App of Apps support
- Git write-back support
- Cluster View - Card view of a cluster that includes all current objects (apps/tools)
- Able to delete child accounts
- Tags delete support
- Forgotten password support
- User controlled Agent version updates
- Add 'warning' status to worstStatus calculation in AppDefinitionsProcessor (f27c5e7)
- Add isManuallyTriggered flag to CreateUsageReportInput (#1501) (9ee3052)
- alertRules: Update relativeTimeRange in alert rule templates to 60 seconds (#1392) (e59e7d5)
- api: Add AlertSummariesModule to the API (#1276) (9b09b7f)
- appDefinitions: Add version field (#1503) (d8dea2a)
- app: Improve validation for RFC 1123 and RFC 1035 standards (#1393) (852ce11)
- applications: Add option to filter by clusterId and derivedKind (#1504) (511127c)
- auth: Add email field to jwt payload for refreshJwt (#1408) (0acf84c)
- auth: Displaying oauth provider on frontend (#1452) (34d9ecd)
- auth: Oauth setup using google and github (#1369) (96260e6)
- auth: Update password reset functionality (#1379) (6229e0f)
- Change updateCluster(not attached) to clear out ingress data (#1417) (997e651)
- clusters: Adding 'ingressAddress' field to cluster DTos and model (#1547) (b306209)
- clusters: publicAddress field support (#1561) (ea69e7c)
- clusters: UsesIngress handler (#1534) (63a4452)
- iacs: Delete child apps in 1h when IAC marked as inactive (#1448) (610f98d)
- network: Add velero appDefinition (#1445) (4fa80ab)
- networkFeatures: kubernetes dashbaord (#1564) (ed3f852)
- networks: Add cleanup logic for network resources during deletion (#1426) (9404477)
- Rename alertRule to alertRuleDefinition (#1377) (68af8ed)
- reports: Add user reports (#1485) (d7aac55)
- repository: Improve update operation performance and error handling (#1461) (a8a4da4)
- system-events: Add clusterId and networkId filters (#1529) (9f42245)
- system-events: Add module (#1431) (1db77e8)
- Update ArgoSyncStatus mapping to include 'warning' status (#1436) (3cfb91d)
- Update cluster service updateAttached to handle hub-specific fields (#1387) (2747229)
- Update validation for Application Definition name length (#1497) (3f878cc)
- users: User account suspension and teardown (#1512) (f05f21b), closes #1514
- velero-volume-snapshot-locations: Add module (#1472) (d1b867c)
- whitelabel: Extend White label Functionality for Frontend Redirects and Backend Emails (#1468) (b5dca2b)

# Improvements
- Enhanced Network Scope experience on all pages
- Network Delete and Force Delete enhanced to show resources being deleted
- Enhanced DNS Check on Ingress types Hubs
- Network Hub IP/Network configuration is now editable (without deleting Network)
- IaC, Terraform workspace conditions are now available in Application Resource tree.


# Bug fixes
- appDefs: Fix application and cluster name validation typos to comply with RFC standards (#1406) (5f9d16e)
- applications: Update ApplicationsListFilterInput type to use DerivedKind (enum) (#1519) (ff7cf82)
- auth: Add error handling for user not found in AuthService (#1459) (97671d4)
- auth: Add null check for referer in extractWhiteLabelFromReferer function (#1516) (fdeb8a9)
- auth: Adding display name to email sent for password reset (#1397) (3c71530)
- auth: Improved error handling for oauth processes. (#1398) (d40663e)
- clusters: Null shutdown field on attachement (#1528) (620aeaa)
- networkFeature: fixed casing on app (#1565) (e538c45)
- networks: Add error handling for cluster detachment on softDelete (#1438) (737ce4a)
- networks: Fix for K8s Dashboard Network Feature (#1567) (e19cdbf)
- oauth: Handling github display name edge case (#1395) (740f33c)
- repository: Check and override null fields for dot notated (nested) updates (#1435) (045ffe9)
- usage-reports: Fix situation when there is missing data in db (#1518) (60f34ce)
- whitelabels: Adding Excluded Url Keywords to fix white-label redirect bug (#1531) (912344c)


# Known issues

# Deprecated features

- Argo Events and Workflows are not currently supported in this release. The plan is to re-incorporate them back into KAOPS upon customer request.
- Nethopper Alerts removed and will be replaced by Grafana Alerts in 6.2
- Cluster kubectl terminal remove and will be replaced by Kubernetes Dashboard in 6.2