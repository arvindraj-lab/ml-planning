---
name: DLaaS PDP template
about: This epic template should be used DLaaS Production Deployment Plan (PDP)

---
# Deep Learning as a Service (DLaaS) Production Deployment Plan (PDP)

## Deployment description:
< Add a high description of the changes e.g. security fixes, BOM updates, add features X,Y,Z including links to the corresponding issues>

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
- Dev: <Link to Report\>
- Staging: <Link to Report\>
- WML-SMOKE SVT: <Link to Report\>
  - <Copy of actual results including passed/failed\>

## Production Deployment Checklist

## Document the steps you used to deploy this change
1. Use the [DeployAll Jenkins Job](https://watson-tron-jenkins.swg-devops.com/job/dlaas-retail/job/deployAll/job/deploy/) with the following options:

| Microservice   | Requirement | Version       |
| -------------- | ----------- | ------------- |
| Learner Config | <YES/No>    | <blank/`<master-xyz>` |
| LCM            | <YES/No>    | <blank/`<master-xyz>` |
| Trainer        | <YES/No>    | <blank/`<master-xyz>` |
| TDS            | <YES/No>    | <blank/`<master-xyz>` |
| Ratelimiter    | <YES/No>    | <blank/`<master-xyz>` |
| DVT            | <YES/No>    | <blank/`<master-xyz>` |

2. Other steps as required (non-Jenkins steps)

## Document the steps to roll back the change if there is an issue
1. Use the [DeployAll Jenkins Job](https://watson-tron-jenkins.swg-devops.com/job/dlaas-retail/job/deployAll/job/deploy/) with the following options:

| Microservice   | Requirement | Version       |
| -------------- | ----------- | ------------- |
| Learner Config | <YES/No>    | <blank/`<master-xyz>` |
| LCM            | <YES/No>    | <blank/`<master-xyz>` |
| Trainer        | <YES/No>    | <blank/`<master-xyz>` |
| TDS            | <YES/No>    | <blank/`<master-xyz>` |
| Ratelimiter    | <YES/No>    | <blank/`<master-xyz>` |
| DVT            | <YES/No>    | <blank/`<master-xyz>` |

### Production Retail
- [ ] prdwat_dal10_cruiser5_retail 
- [ ] prdwat_lon04_cruiser2_retail

### Deployment logs 
(Added as a seperate comment -- not in description)
- < copy of Deployment Logs for each cluster > 

### Backout logs (if applicable) 
(Added as a seperate comment -- not in description)
- < Backout Logs for each cluster (if applicable) > 

## Approvals
(Added as a seperate comment -- not in description)
- Dev representative **->** <Add comment stating "I have reviewed and I approve.">
- QA representative **->** <Add comment stating "I have reviewed and I approve.">
- DevOps representative **->** <Add comment stating "I have reviewed and I approve.">
