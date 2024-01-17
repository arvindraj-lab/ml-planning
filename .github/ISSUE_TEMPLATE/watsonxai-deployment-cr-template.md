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
|watsonx inference proxy       | wx-inference-proxy            | x.x.x | Dallas and Frankfurt DC Only |
|fmaas-router                  | fmaas-router                  | x.x.x | Washington and Frankfurt DC only |
|foundation models             | fmaas-runtime-wisdom-ansible  | x.x.x | Washington and Frankfurt DC only |
|bamdev-cais                   | pod-coordinator               | x.x.x | Washington and Frankfurt DC only |
|bamdev-cais                   | caikit-nlp-service-trainer    | x.x.x | Washington and Frankfurt DC only |
|caikit-runtime-stack-operator | caikit-runtime-stack-operator | x.x.x | Washington and Frankfurt DC only |
|fmaas-caikit-inf-prompt-tunes | caikit-nlp-service-trainer    | x.x.x | Washington and Frankfurt DC only |
|fmaas-caikit-trainer          | caikit-nlp-service-trainer    | x.x.x | Washington and Frankfurt DC only |
|fmaas-mt                      | lifecycle-manager-service     | x.x.x | Washington and Frankfurt DC only |
|fmaas-mt                      | trainer-v2-service            | x.x.x | Washington and Frankfurt DC only |

## Other Tasks

Copy Watsonx.ai images using [Watsonx_Image_Push_to_Registry](http://jenkins-wml-server1.fyre.ibm.com:8080/job/Watsonx_Image_Push_to_Registry/)
Copy inference-proxy image using [move_image_fromStaging_toProd](http://jenkins-wml-server1.fyre.ibm.com:8080/job/move_image_fromStaging_toProd/)

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

Jenkins VA Scan: http://jenkins-wml-server1.fyre.ibm.com:8080/job/WML-Image-Vulnerability-Check-CR/
