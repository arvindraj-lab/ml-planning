---
name: Watsonx.ai CR Template
about: This template should be used to request a change in the `watsonx.ai` limits for specific instance IDs
title: 'Watsonx.ai CR Content for Week of <Month Day Year>'
labels: Watsonx.ai-CR
assignees: tamdavid
---

## Environment Details
Non-disruptive Deployment: YES

YPCR: <Month Day Year>
YP: <Month Day Year>

Assigned Resource: 

## Summary of Changes
1. 

## Build and Deployment Details

Runbooks and Deployment Steps Details: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

|Service Name|Image Name|Version|Remarks|
|----------------|----------------|---------|-----|
|WML Inference Proxy|wx-inference-proxy| x.x.x |Dallas and Frankfurt DC Only|
|Watsonx.ai Router|fmaas-router| x.x.x |Washington and Frankfurt DC only|
|Watsonx.ai TGIS|fmaas-runtime-wisdom-ansible| x.x.x |Washington and Frankfurt DC only|
|COS Driver|N/A| x.x.x |Washington and Frankfurt DC only|

## Other Tasks

### YPCR
- [ ] PR: [Description](Link to PR)
- [ ] PR: [Description](Link to PR)

### Prod
- [ ] PR: [Description](Link to PR)
- [ ] PR: [Description](Link to PR)

Deploy changes using [Deploy-WatsonX-Services](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/Deploy-WatsonX-Services/)

## Backout Plan

For microservices to recover re-deploy previous version https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

## VA Scan Results

Link to VA Scan: URL
