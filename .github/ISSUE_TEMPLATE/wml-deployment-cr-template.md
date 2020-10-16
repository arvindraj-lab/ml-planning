---
name: WML Deployment CR template
about: Template to create the WML CR content
title: Microservices CR content for the week of <Month Date Year e.g June 8th 2020
  >
labels: ''
assignees: ''

---

Environment Details
Non-disruptive deployment:

YS1 : 
YP Dallas, YP Frankfurt, YP tokyo, YP London -->

Assigned Resource  : 

### Summary of Contents in new CR
1. 
2.
3.




### FVT Details
FVT env: This change was successfully deployed on
FVT env: Automated regression testing status:
Microservices:
- Online Scoring:
* Spark / PMMLRuntime v3: 
* Python (Scikit / XGBoost) : 
* Python (TF/Keras) : 
* Python (Caffe):  
* Decision Optimzation
* Functions Runtime v3: 
* Runtime Manager v3: 
* Envoy: 
* Agent: 
* Hybrid Runtime: 
* Spss Runtime: 
- Batch Scoring v2 (Spark):  
- Streaming: No Change
- Repository: 
- Ingestion:
- Token:
- ML Deployment: 
- ML Online Feedback:
- ML Event Consumer:
- WML Instances:
- Training:
- Operations Service
FVT env: Specific testing has been run that validates the change is successful?




### SVT Details
SVT env: This change was successfully deployed on
SVT: Automated regression testing status:
a) Microservices:
- Online Scoring:
- Batch Scoring:
- Streaming:
- Ingestion:
- Repository:
- Token:
- ML Deployment:
- ML Online Feedback:
Training
- Experiments:
- Deep Learning:
- Pipelines v3:
- Pipelines v2:
Stress Test Result Link
- Stress v3:
- *Stress v3 (Spark):
- *Stress v2:
SVT env: Specific testing has been run that validates the change is successful?




### Build and Deployment Details
Scoring v3 (Includes Online v3 and Batch v3):
* Spark / PMMLRuntime v3:
- Version 2.1 - 
- Version 2.3 - 
* Python (Scikit / XGBoost) Runtime v3: 
* Python (TF/Keras) Runtime v3: 
* Python (Caffe) Runtime v3: 
* Functions Runtime v3: 
* Runtime Manager v3: 
* Envoy: No Change
* Agent: No Change
* Hybrid Runtime: 
* Spss Runtime: 
* Decision optimization

runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

Batch Scoring v2 (Spark)
version: 
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

Streaming
version: No Change
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

Repository
version: 
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

ML Deployment
version:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

ML Online Feedback
version:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

ML Event Consumer
version:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

WML Instances
version:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

Training
version: 
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

Ingest
version:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

Token
version:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md

WML Proxy
config:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_ Deploy_Steps.md

Operations service
version:
runbook: https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_Steps.md



### Other Tasks
Scoring:
1. Any yaml changes in Runtime manager yaml.
2. Any configmap changes getting in and if its delivered in wml-ops before refreshing
Runtime Manager.(Mention PR)
3. Any runtimConfig json file update is required in ETCD.
4. Any new ETCD keys has to be added when a new feature is going in.
5. Any exisiting ETCD records has to be migrated.
6. Any new pvc has to be created.
7. Any specific sequence has to be followed to update RM,Envoy,Runtimes and Agent                                                                                              
8. Any new endpoints has to be enabled in nginx                                                                                                                                                            
9. Any vault secrets or ETCD details has to edited in kubesecrets. 




### WML Python Client:

### Backout Plan
 For microservices to recover re-deploy previous version https://github.ibm.com/cds-devops/NGP-runbook/blob/master/deployments/WML_Prod_Deploy_
