---
name: DLaaS PDP template
about: This epic template should be used DLaaS Production Deployment Plan (PDP)
title: ''
labels: wml-dlaas
assignees: ''

---

# Deep Learning as a Service (DLaaS) Production Deployment Plan (PDP)

## Deployment Description:
- < Add a high description of the changes e.g. security fixes, BOM updates, add features X,Y,Z including links to the corresponding issues>

## Desired Target Deployment Date
- < MM-DD-YYYY >

## Content 
### Image/Content(s) that changed
- `<List of changed microservices (if any)>`

### Vulnerability Advisor Scan Results
- <Listing of clean VA scan results for included images\>

### Build logs
- < Genkins build logs>

### Test logs

**NOTE: DVT NOT REQUIRED IF NO MICROSERVICE OR LEARNER UPDATES**
- DVT Test Dev: <Link to Report\>
- DVT Test Staging: <Link to Report\>
- WML-SMOKE SVT Staging: <Link to Report\>
    ```
    <Copy of actual results including passed/failed\>
    ```

## Deployment Instructions

**REMOVE IF NOT UPDATING MICROSERVICES OR LEARNER IMAGES**
1. Use the [DeployAll Jenkins Job](https://watson-tron-jenkins.swg-devops.com/job/dlaas-retail/job/deployAll/job/deploy/) with the following options:

| Microservice   | Requirement | Version       |
| -------------- | ----------- | ------------- |
| Learner Config | <YES/No>    | <blank/`<master-xyz>` |
| LCM            | <YES/No>    | <blank/`<master-xyz>` |
| Trainer        | <YES/No>    | <blank/`<master-xyz>` |
| TDS            | <YES/No>    | <blank/`<master-xyz>` |
| Ratelimiter    | <YES/No>    | <blank/`<master-xyz>` |
| DVT            | <YES/No>    | <SMOKE/ALL> |

**ONLY REQUIRED IF** `Learner Config=YES` **AND** `LCM=NO`
1. Restart the LCM serviec using the following command.  NOTE: Requires `kubectl 1.15`
    ```
    kubectl -n dlaas rollout restart deployment dlaas-lcm
    ```
    
**REMOVE IF NOT UPDATING COS DRIVER**
1. Update the COS Driver by following the instructions [HOW TO UPDATE THE COS DRIVER](https://github.ibm.com/NGP-TWC/WML-DLaaS/blob/master/HowTo/UpdateCOS.md)

**REMOVE IF NOT UPDATING IKS**
1. Update the IKS Worker Nodes by following the instructions [HOW TO UPDATE KUBERNETES FOR DLAAS](https://github.ibm.com/NGP-TWC/WML-DLaaS/blob/master/HowTo/UpdateIKS.md)

**REMOVE IF NOT UPDATING CSUTIL**
1. Re-run the `csutil` setup by following the instructions [How To Install and Update csutil](https://github.ibm.com/NGP-TWC/WML-DLaaS/blob/master/HowTo/InstallUpdatecsutil.md)

**REMOVE IF NOT UPDATING IKS OR LEARNER IMAGES**
1. Run the learner images caching job in each cluster to pre-cache them on the GPU nodes [How to run the learner image caching](https://github.ibm.com/NGP-TWC/WML-DLaaS/blob/master/HowTo/CacheLearnerImages.md)

## Rollback Instructions

**REMOVE IF NOT UPDATING MICROSERVICES OR LEARNER IMAGES**
1. Use the [DeployAll Jenkins Job](https://watson-tron-jenkins.swg-devops.com/job/dlaas-retail/job/deployAll/job/deploy/) with the following options:

| Microservice   | Requirement | Version       |
| -------------- | ----------- | ------------- |
| Learner Config | <YES/No>    | <blank/`<master-xyz>` |
| LCM            | <YES/No>    | <blank/`<master-xyz>` |
| Trainer        | <YES/No>    | <blank/`<master-xyz>` |
| TDS            | <YES/No>    | <blank/`<master-xyz>` |
| Ratelimiter    | <YES/No>    | <blank/`<master-xyz>` |
| DVT            | <YES/No>    | <SMOKE/ALL> |

**ONLY REQUIRED IF** `Learner Config=YES` **AND** `LCM=NO`
1. Restart the LCM serviec using the following command.  NOTE: Requires `kubectl 1.15`
    ```
    kubectl -n dlaas rollout restart deployment dlaas-lcm
    ```

**REMOVE IF NOT APPLICABLE**
1. IKS downgrade not supported.

1. COS driver downgrade not supported.

1. csutil downgrade not supported.

## Production Deployment Checklist

### Production Retail
- [ ] prd-wml-dl-dal-cluster1
- [ ] prd-wml-dl-fra-cluster1

### Deployment logs 
(Added as a seperate comment -- not in description)
- < copy of Deployment Logs for each cluster > 

### Backout logs (if applicable) 
(Added as a seperate comment -- not in description)
- < Backout Logs for each cluster (if applicable) > 

## Approvals
(Added as a seperate comment -- not in description)
- Dev representative **->** <Add comment stating "I have reviewed and I approve for Dev.">
- QA representative **->** <Add comment stating "I have reviewed and I approve for QA.">
- DevOps representative **->** <Add comment stating "I have reviewed and I approve for DevOps.">

## Change Request
Create a [Watson Machine Learning CR](https://github.ibm.com/NGP-TWC/WDP-Deployments/issues/new/choose) and include link here.
