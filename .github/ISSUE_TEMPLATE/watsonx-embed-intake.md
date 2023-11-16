---
name: watsonx.ai embed intake form
about: This template should be used to request to embed watsonx.ai 
title: 'watsonx.ai embed intake form for [product name + feature]'
labels: watsonx
assignees: demi-ajayi 
---

### watsonx.ai embed intake
All IBM teams planning to integrate watsonx.ai for production should start with this template, and begin the process as soon you begin planning your feature release. 

You may not have all information needed right now, but submit this form so we can get started. We will add relevant information as it becomes available. 

Filling this form is a not a commitment from the watsonx.ai but allows us to track incoming requests. 

#### 1. Product team:

#### 2. Product proposed Feature GA Date: 

 This date must be agreed to by watsonx.ai team and product team. We will not commit to a GA date we haven’t approved and been apprised of ahead time with proper dev planning from both teams. 

#### 3. Delivery type:

calling 

- [ ] watsonx.ai on IBM Cloud 
- [ ] watsonx.ai on-prem

product is hosted on: 

#### 4. Release type:
- [ ] Internal Experimenting - Please use BAM 
- [ ] Private Preview 
- [ ] Public Preview 
- [ ] GA

For:
- [ ] internal IBM use (by IBMers)
- [ ] external client use (product release)
- [ ] external client engagement (client engagement)


#### 5. watsonx.ai Python SDK

All IBM teams going into production must use the [watsonx.ai Python SDK](https://ibm.github.io/watson-machine-learning-sdk/install.html) until the GA of the watsonx.ai APIs (currently in beta).

- [ ] Our product is using the SDK for our release

#### 6. Model:

Full name of model team intends to use: [example granite.13b.chat-v1 ]

DCT number:

Model is: 
- [ ] existing model on watsonx.ai API - public 

- [ ] new base model on watsonx.ai roadmap - public

- [ ] fine-tuned model for just your product (hidden)

- [ ] fine-tuned model used by other IBM product (hidden)

copy section 6 for each model used in this feature. 

#### 7. If model(s) is/are hidden: 
- fill out this [Github ticket](https://github.ibm.com/NGP-TWC/ml-planning/issues/new?assignees=julianpayne&labels=WML-BYOM%2Cwatsonx%2Cwatsonx-inference-proxy%2Cwatsonx-fm-dev%2CdevOps&template=wml-byom-onboarding.md&title=watsonx.ai+onboarding+request) 
- follow [these instructions](https://ibm.ent.box.com/notes/1349751157331?s=bbp3rbdt29q81mqpci3ylopz43t1zc2b) for relevant information needed for supporting hiding model.
- add the github links to this issue.


Please specify  the above for each model to be used


Note: relevant model clearances are needed and are the responsibility of the product team to check and obtain necessary approvals with model owners in DCT



#### 8. Capacity Usage:

Provide usage projections for each model used in this feature. This is used for GPU allocation & very important



Provide on a quarterly basis for next 4 quarters from release:

Provide accessible link to calculations - 

- Model:
- Data center : [date center requested] 

Output:
 - projected input tokens per month per model for this use case: 
 - peak api requests/hour: (if any surge usage is expected)

input:
-  Number of users:
-  api requests per month
-  tokens per api request per user

copy section 8 for each model used in this feature.

#### 9. Performance

[Latency requirements if applicable]

[rate limits requirements if applicable]


#### 10. Aha!
Provide a link to your corresponding Aha! epic for this feature here:

Please be sure it includes (or include below):

- Feature Description (with relevant user stories): 


#### 11. Next steps

Thanks for filling this form. The watsonx.ai embed will review this issue and your Aha! epic and track the dependency in our [dependency report](https://ibm.biz/watsonxai-embed-dependency-report). 
We'll be in touch to schedule your intake meeting.
See our full process and policy here.  

