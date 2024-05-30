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
|watsonx inference proxy       | wx-inference-proxy                     | x.x.x | All 4 DCs |
|fmaas-embeddings-router       | fmaas-router                           | x.x.x | All 4 DCs |
|FM - tgis                     | quay.io/modh/text-generation-inference | x.x.x | All 4 DCs |
|FM - vllm                     | quay.io/wxpe/tgis-vllm                 | x.x.x | All 4 DCs |
|bamdev-cais                   | pod-coordinator                        | x.x.x | All 4 DCs |
|bamdev-cais                   | caikit-nlp-service-trainer             | x.x.x | All 4 DCs |
|caikit-runtime-stack-operator | caikit-runtime-stack-operator          | x.x.x | All 4 DCs |
|fmaas-caikit-inf-prompt-tunes | caikit-nlp-service-trainer             | x.x.x | All 4 DCs |
|fmaas-caikit-trainer          | caikit-nlp-service-trainer             | x.x.x | All 4 DCs |
|fmaas-mt                      | lifecycle-manager-service              | x.x.x | All 4 DCs |
|fmaas-mt                      | trainer-v2-service                     | x.x.x | All 4 DCs |

## Other Tasks

Copy Watsonx.ai images using [Watsonx_Image_Push_to_Registry](http://jenkins-wml-server1.fyre.ibm.com:8080/job/Watsonx_Image_Push_to_Registry/)
Copy inference-proxy image using [move_image_fromStaging_toProd](http://jenkins-wml-server1.fyre.ibm.com:8080/job/move_image_fromStaging_toProd/)

### YPCR
--- REMOVE Cert Regenerate if not first CR of each month ---
- [ ] Run [Cert Regenerate](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/watsonx-cert-regenerate/) in YS1
- [ ] Run [Cert Regenerate](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/watsonx-cert-regenerate/) in YPQA
--- REMOVE Cert Regenerate if not first CR of each month ---
- [ ] PR: [Description](Link to PR)
- [ ] PR: [Description](Link to PR)

### Prod
--- REMOVE Cert Regenerate if not first CR of each month ---
- [ ] Run [Cert Regenerate](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/watsonx-cert-regenerate/) in WDC
- [ ] Run [Cert Regenerate](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/watsonx-cert-regenerate/) in FRA
- [ ] Run [Cert Regenerate](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/watsonx-cert-regenerate/) in TOK
- [ ] Run [Cert Regenerate](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/watsonx-cert-regenerate/) in LON
--- REMOVE Cert Regenerate if not first CR of each month ---
- [ ] PR: [Description](Link to PR)
- [ ] PR: [Description](Link to PR)

Deploy changes using [Deploy-WatsonX-Services](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/Deploy-WatsonX-Services/)

### Post Deployment Verification
- [ ] Run [Test All Models](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Models/) in DAL - PUT JOB LINK HERE
- [ ] Run [Test All Prompt Tuning](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Prompt-Tuning/) in DAL - PUT JOB LINK HERE
- [ ] Run [Test All Models](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Models/) in FRA - PUT JOB LINK HERE
- [ ] Run [Test All Prompt Tuning](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Prompt-Tuning/) in FRA - PUT JOB LINK HERE
- [ ] Run [Test All Models](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Models/) in TOK - PUT JOB LINK HERE
- [ ] Run [Test All Prompt Tuning](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Prompt-Tuning/) in TOK - PUT JOB LINK HERE
- [ ] Run [Test All Models](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Models/) in LON - PUT JOB LINK HERE
- [ ] Run [Test All Prompt Tuning](https://hyc-wml-devops-team-jenkins.swg-devops.com/job/WatsonX-Test-All-Prompt-Tuning/) in LON - PUT JOB LINK HERE

## Backout Plan

For microservices to recover re-deploy previous version https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

## VA Scan Results

Jenkins VA Scan: http://jenkins-wml-server1.fyre.ibm.com:8080/job/WML-Image-Vulnerability-Check-CR/
