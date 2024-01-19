---
name: watsonx.ai embed intake form
about: This template should be used to request to embed watsonx.ai 
title: 'watsonx.ai embed intake form for [product name + feature]'
labels: watsonx,embed
assignees: Demi-Ajayi 
---

### watsonx.ai embed intake

All IBM teams planning to integrate watsonx.ai for production should start with this template, and begin the process as soon you begin planning your feature release.

You may not have all information needed right now, but please submit this form so we can get started. We will add relevant information as it becomes available.

Filling this form is a not a commitment from the watsonx.ai but allows us to track incoming requests.

#### 1. Product team:

#### 2. Product proposed Feature Release Date:

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

#### 5. watsonx.ai API & Python SDK

All IBM teams are highy encouraged to go into production with the [watsonx.ai Python SDK](https://ibm.github.io/watson-machine-learning-sdk/install.html) until the GA of the watsonx.ai APIs (currently in beta).

- [ ] Our product will use the Python SDK for our release
- [ ] Our product will use the Beta API for our release and are aware there will be breaking changes for the GA and potentially for other updates before GA. 

Please have your developers join our slack channel for updates: #delivering-llms-in-product-in-2023

API endpoint used:

- [ ] text/generation (generation/text)
- [ ] text/generation_stream (generation/text_stream)

#### 6. Model:

Full name of model team intends to use (example granite.13b.chat-v1):

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

#### 8. Tracking Usage

BSS ID:

watsonx.ai Plan Type (for production associated with BSS ID):
- [ ] Essentials Plan
- [ ] Standard Plan 

Please follow instructions [here](https://w3.ibm.com/w3publisher/using-llms-ibm/delivery-playbook/cost-tracking-getting-started) to provide the correct BSS ID. This will be used to allow-list your product to avoid billing charges in production. 



#### 9. Usage Projection

Provide usage projections for each model used in this feature. This is used for GPU allocation & very important

Provide on a quarterly basis for next 2 quarters from release:

Provide accessible link to calculations -

- Model:
- Data center:

Output:

- projected input tokens per month per model for this use case: 

Input:

- Number of users:
- api requests per month:
- tokens per api request per user:

copy section 9 for each model used in this feature.

#### 10. Performance

Latency requirements if applicable:

rate limits requirements if applicable:

#### 11. Aha!

Provide a link to your corresponding Aha! epic for this feature here:

Please be sure it includes (or include below):

- Feature Description (with relevant user stories): 

#### 12. Next steps

Please join our slack channel: (search)- #delivering-llms-in-product-in-2023 to stay tuned for important updates 

Thanks for filling this form. The watsonx.ai embed will review this issue and your Aha! epic and track the dependency in our [dependency report](https://ibm.biz/watsonxai-embed-dependency-report).
We'll be in touch to schedule your intake meeting.
Learn more about our full process [here.](https://w3.ibm.com/w3publisher/using-llms-ibm/delivery-playbook)  

@Demi-Ajayi

#### 13. For watsonx.ai team only
- [ ] BSS ID validated
- [ ] Business Case approved
- [ ] product submitted to allow-list

