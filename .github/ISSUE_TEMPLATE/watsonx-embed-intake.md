---
name: watsonx.ai embed intake form
about: This template should be used to request to embed watsonx.ai 
title: 'watsonx.ai embed intake form'
labels: watsonx
assignees: demiajayi otucker 


### watsonx.ai embed intake
All IBM teams planning to integrate watsonx.ai for production should start with this template, and begin the process as soon as possible. Please fill this out to the best of your knowledge. Filling this form is a not a commitment from the watsonx.ai but allows us to track incoming requests. 

#### Product team:

#### Product proposed Feature GA Date: 

 This date must be agreed to by watsonx.ai team and product team. We will not commit to a GA date we haven’t approved and been apprised of ahead time with proper dev planning from both teams. 

#### Delivery type:

calling 

- [ ] watsonx.ai on IBM Cloud 
- [ ] watsonx.ai on-prem

product is hosted on: 

#### Release type:
- [ ] Experimental/Tech Preview
- [ ] Beta
- [ ] GA

For:
- [ ] internal IBM use (by IBmers)
- [ ] external client use (product release)
- [ ] external client engagement (client engagement)


#### Beta API Disclaimer:

Our current watsonx.ai API is in beta, and does not have version dates, etc. The GA API is on the roadmap. As such breaking changes will be documented and communicated to teams with a committed dependency on watsonx.ai via 

- [ ] Team has been made aware & consented to use of watsonx.ai beta API with potential breaking changes, which will be documented by watsonx team

#### Model:

Full name of model team intends to use: [example granite.13b.chat-v1 ]

Model is: 
- [ ] existing model on watsonx.ai API - public 

- [ ] new base model on watsonx.ai roadmap - public

- [ ] fine-tuned model for just your product (hidden)

- [ ] fine-tuned model used by other IBM product (hidden)

 

- [ ] If model(s) is/are hidden 
- fill out this [Github ticket](https://github.ibm.com/NGP-TWC/ml-planning/issues/new?assignees=julianpayne&labels=WML-BYOM%2Cwatsonx%2Cwatsonx-inference-proxy%2Cwatsonx-fm-dev%2CdevOps&template=wml-byom-onboarding.md&title=watsonx.ai+onboarding+request) 
- follow [these instructions](https://ibm.ent.box.com/notes/1349751157331?s=bbp3rbdt29q81mqpci3ylopz43t1zc2b) for relevant information needed for supporting hiding model.
- add the github links to this issue.


Please specify for each model to be used
Fill the following for each model that will be used
Note: relevant model clearances are needed and are the responsibility of the product team to check and obtain necessary approvals with model owners in DCT



#### Capacity Usage:

Provide usage projections for each model used. This is used to requirements

- Model:

- Usage for model [ name]:
provide projection of
-  Number of users:
-  tokens per month
-  api requests per month
-  peak api usage
on quarterly basis out for 1 calendar year
Provide link to calculations - 
- Data center : [date center requested] for [model]

#### Performance

[Latency requirements if applicable]

[rate limits requirements if applicable]


#### Aha!
Provide a link to your corresponding Aha! epic for this feature here:

#### Feature

[Description of feature, with relevant user stories]


#### Requirements for Watsonx

Please provide as much detail on requirements on watsonx.ai. If you only have high level requirements, that's fine = we will scope this out together.


#### Next steps

Thanks for filling this form. The watsonx.ai embed will review this issue and your Aha! epic and track the dependency in our [dependency report[(https://ibm.biz/watsonxai-embed-dependency-report). 
We'll be in touch to schedule your intake meeting.
See our full process and policy here.  

