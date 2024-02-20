---
name: Watsonx.ai model lifecycle request
about: This template should be used to request a definition of lifecycle plans for `watsonx.ai` models, or to request a change in such plans
title: 'watsonx.ai model lifecycle request'
labels: watsonx-models-lifecycle-request,watsonx-fm-dev,watsonx
assignees: aronovic,tamdavid
---

## Request to define or change lifecycle plans for `watsonx.ai` models in cloud or onprem

### Request details (to be completed by the requester)

1. Context of the request: ...
1. Links to related issues: ...

For each model ID requested for defining or changing a lifecycle plan, specify the following details.  
Please include multiple models whose lifecycle plans should be processed together - into one request.  
Fill out only the states that are requested to be included in the lifecycle plan for the model.  
Fill out only the information that is needed for `cloud` or for `onprem`, depending on the type of request.  

1. Model ID: ...
1. [cloud] Environments: ...  
   {List of environments in which to apply the lifecycle plan for the model. If this should be applied in all the current environments where the model is available - specify "all".}
1. Request type (choose one):
   - [ ] New definition of a lifecycle plan.
   - [ ] Change in an existing lifecycle plan.
1. [ ] List of recommended alternative model IDs [optional]: ...  
   {For requests that include deprecation and / or constriction, this is a comma separated list of IDs of alternative models which are recommended to be used instead of this model.}
1. [ ] **Availability state specification**:  
   {This section specifies a general availability state for the model.}
   1. [cloud] Start date: ...  
      {Date when the general availability state starts.}
   1. [onprem] Since version: ...  
      {Version since which the general availability state starts.}
1. [ ] **Deprecation state specification**:  
   {This section specifies a deprecation state for the model, where the model is available without restrictions, and a warning is returned for calls for this model. For cloud, this state must be followed by at least one of the following states.}
   1. [cloud] Start date: ...  
      {Date when the deprecation state starts.}
   1. [onprem] Since version: ...  
      {Version since which the deprecation state starts.}
   1. URL [optional]: ...  
      {URL for documentation that is specific for this model's deprecation state.}
1. [ ] **Constriction state specification**:  
   {This section specifies a constriction state for the model, where the model is no longer available in the tuning APIs, and is still available in the inference APIs. Inference calls for this model return a warning.}
   1. [cloud] Start date: ...  
      {Date when the constriction state starts.}
   1. [onprem] Since version: ...  
      {Version since which the constriction state starts.}
   1. URL [optional]: ...  
      {URL for documentation that is specific for this model's constriction state.}
1. [ ] **Withdrawn state specification**:  
   {This section specifies a date or version from which the model is withdrawn. In cloud, all API calls for this model are rejected, and the actual model should not be present in the back-end environment from this date. In onprem, inference API calls for this model are still allowed, but the model is no longer supported by IBM.}
   1. [cloud] Start date: ...  
      {Date when the withdrawn state starts.}
   1. [onprem] Since version: ...  
      {Version since which the withdrawn state starts.}
   1. URL [optional]: ...  
      {URL for documentation that is specific for this model's withdrawn state.}

### Request processing (to be completed by the watsonx.ai team)

#### Models configuration

- [ ] Prepare PRs for the requested changes in the relevant environments.

Cloud:

- [ ] Add the PRs to the relevant CR issues.  
- [ ] Fill out the tables below.

Onprem:

- [ ] Add the PRs to an onprem build.

#### Devops

[ ] Apply the operations specified in the table below to the back-end environments by the requested dates.

Completion indication|Model ID|Environment|Operation (`Remove` or `Ensure availability`)|Date to apply the operation
--|--|--|--|--
[ ]|example/model_id|prod dallas|remove|example_date

#### Administrative

- [ ] When all the operations above are complete, close this ticket.  
- [ ] Periodically remove models that are already in the withdrawn state from the wx-inference-proxy models configuration.  

CC: @aronovic @otucker @pvanrun
