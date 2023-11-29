---
name: Watsonx.ai model lifecycle request
about: This template should be used to request a definition of lifecycle plans for `watsonx.ai` models, or to request a change in such plans
title: 'watsonx.ai model lifecycle request'
labels: watsonx-models-lifecycle-request,watsonx,watsonx-fm-dev
assignees: otucker aronovic pvanrun tamdavid
---

## Request to define or change lifecycle plans for `watsonx.ai` models in public cloud

### Request details (to be completed by the requester)

1. Context of the request: ...
1. Links to related issues: ...

For each model ID requested for defining or chaning a lifecycle plan, specify the following details.  
Fill out only the stages that are requested to be included in the lifecycle plan for this model.

1. Model ID: ...
1. Environments: ...  
   {List of environments in which to apply the lifecycle plan for the model. If this should be applied in all the current environments where the model is vailable - specify "all".}
1. Request type (choose one):
   - [ ] New definition of a lifecycle plan.
   - [ ] Change in an existing lifecycle plan.
1. [ ] List of recommended model IDs [optional]: ...  
   {For requests that include deprecation, this is a comma separated list of IDs of other models which are recommended to be used instead of this model.}
1. [ ] **Availability stage specification**:  
   {This section specifies a general availability period for the model.}
   1. Start date: ...  
      {Date when the general availability period starts.}
1. [ ] **Deprecation stage specification**:  
   {This section specifies a deprecation period for the model, where the model is available without restrictions, and a warning is returned for calls for this model. This stage must be followed by at least one of the following stages.}
   1. Start date: ...  
      {Date when the deprecation period starts.}
   1. URL [optional]: ...  
      {URL for documentation that is specific for this model's deprecation stage.}
1. [ ] **Constriction stage specification**:  
   {This section specifies a constriction period for the model, where the model is no longer available in the tuning APIs, and is still available in the inferencing APIs. Inference calls for this model return a warning.}
   1. Start date: ...  
      {Date when the constriction period starts.}
   1. URL [optional]: ...  
      {URL for documentation that is specific for this model's constriction stage.}
1. [ ] **Withdrawn stage specification**:  
   {This section specifies a date from which the model is withdrawn. All API calls for this model are rejected. The actual model should not be present in the back-end environment from this date.}
   1. Start date: ...  
      {Date when the withdrawn period starts.}
   1. URL [optional]: ...  
      {URL for documentation that is specific for this model's withdrawn stage.}

### Request processing (to be completed by the watsonx.ai team)

#### Models configuration

1. [ ] Prepare PRs for the requested changes in the relevant environments.
1. [ ] Add the PRs to the relevant CR issues.
1. [ ] Fill out the tables below.

#### Devops

[ ] Apply the operations specified in the table below to the back-end environments by the requested dates.

Completion indication|Model ID|Environment|Operation (`Remove` or `Ensure availability`)|Date to apply the operation
--|--|--|--|--
[ ]|example/model_id|Prod Dallas|Remove|example_date

#### Documentation and UI

[ ] Apply the operations specified in the tables below by the requested dates.

<ins>Deprecation announcements</ins>

Completion indication|Model ID|Requested date
--|--|--
[ ]|example/model_id|example_date

<ins>Archive / remove model assets and references</ins>

Completion indication|Model ID|Requested date
--|--|--
[ ]|example/model_id|example_date

#### Administrative

[ ] When all the operations above are complete, close this ticket.  
[ ] Periodically remove models that are already in the withdrawn stage from the wx-inference-proxy models configuration.  

CC: @otucker @aronovic @pvanrun @tamdavid
