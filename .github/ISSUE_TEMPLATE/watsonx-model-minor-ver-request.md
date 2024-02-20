---
name: Watsonx.ai model minor version request
about: This template should be used to request a definition of minor version plans for `watsonx.ai` models, or to request a change in such plans
title: 'watsonx.ai model minor version request'
labels: watsonx-models-lifecycle-request,watsonx-fm-dev,watsonx
assignees: aronovic,tamdavid
---

## Request to define or change minor version plans for `watsonx.ai` models in cloud

### Request details (to be completed by the requester)

1. Context of the request: ...
1. Links to related issues: ...

For each model ID requested for defining or changing a minor version plan, specify the following details.  
Please include multiple models whose plans should be processed together - into one request.  

1. Model ID: ...
1. Environments: ...  
   {List of environments in which to apply the minor version plan for the model. If this should be applied in all the current environments where the model is available - specify "all".}
1. Full version identifier of the minor version to be applied: ...
1. Date from which the above minor version should be activated: ...
1. URL or description of the contents of the above minor version: ...

### Request processing (to be completed by the watsonx.ai team)

#### Models configuration

- [ ] Prepare PRs for the requested changes in the relevant environments.
- [ ] Add the PRs to the relevant CR issues.
- [ ] Fill out the tables below.

#### Devops

[ ] Apply the operations specified in the table below to the back-end environments by the requested dates.

Completion indication|Model ID|Environment|Operation|Date to apply the operation
--|--|--|--|--
[ ]|example/model_id|prod dallas|update|example_date

#### Administrative

- [ ] When all the operations above are complete, close this ticket.  

CC: @aronovic @otucker @pvanrun
