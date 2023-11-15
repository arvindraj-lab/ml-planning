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

For each model ID requested for defining or chaning a lifecycle plan, specify the following details:

1. Model ID: ...
1. Environments: ...  
   {List of environments in which to apply the lifecycle plan for the model. If this should be applied in all the current environments where the model is vailable - specify "all".}
1. Request type (choose one):
   - [ ] New definition of a lifecycle plan
   - [ ] Change in an existing lifecycle plan

Fill out only the stages that are requested to be included in the lifecycle plan for this model.

1. [ ] **Deprecation stage specification**:  
   {This section specifies a deprecation period for the model, where the model is active without restrictions and a warning is returned for calls for this model. This stage must be followed by at least one of the replacement stage or the inactive stage.}
   1. Start date: ...  
      {Date when the deprecation period starts.}
1. [ ] **Replacement stage specification**:  
   {This section specifies a replacement period for the model, where the model is no longer active, calls that can be rerouted to a replacement model are rerouted with a returned warning, and calls that cannot be rerouted to a replacement model are rejected. The model can be removed from the back-end environment after this period starts. The back-end environment must have the replacement model deployed and available at the beginning of this period.}
   1. Start date: ...  
      {Date when the replacement period starts.}
   1. Replacement model ID: ...  
      {ID of another model to which eligible calls for this model should be rerouted during the replacement period.}
1. [ ] **Inactive stage specification**:  
   {This section specifies a date from which the model is not active and not rerouting to another model. The actual model should not be present in the back-end environment from this date (or prior if a replacement period was defined).}
   1. Start date: ...  
      {Date when the inactivity period starts.}

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
