---
name: Watsonx.ai limits change request
about: This template should be used to request a change in the `watsonx.ai` limits for specific instance IDs
title: 'watsonx.ai limits change request'
labels: watsonx-limits-change-request,watsonx-fm-dev,watsonx-inference-proxy,watsonx
assignees: otucker aronovic
---

## Request to change `watsonx.ai` limits for instance IDs in public cloud

### Request details (to be completed by the requester)

#### Background

It is possible to reconfigure or disable the following limits for an instance ID:

- `rate_limit`: This limit is specified in terms of the maximum number of requests per second for the instance ID.
- `max_output_tokens`: This is the maximum number of output tokens for an inference request.
- `max_input_tokens`: This is the maximum number of input tokens for an inference request.
- `call_time`: This is the maximum duration for an inference request.
- `token_quota`: Token quota can be either enabled or disabled.

The current limits applied per model and per plan are specified in the `foundation_model_specs` API output:

- Prod Dal: <https://us-south.ml.cloud.ibm.com/ml/v1-beta/foundation_model_specs?version=2023-01-01>.
- prod Fra: <https://eu-de.ml.cloud.ibm.com/ml/v1-beta/foundation_model_specs?version=2023-01-01>.

See the sections `model_limits`​ and `limits`​ in the output.

#### Request

To reconfigure or disable specific limits for specified instance IDs, please provide the following information:

1. Name of customer: ...
1. Background / reason for the request: ...
1. Links to associated tickets: ...
1. Requested date for applying the change:
   - [ ] As soon as possible.
   - [ ] Date: ...
1. Requested date for removing the change:
   - [ ] Indefinite.
   - [ ] Date: ...
1. For each CRN that is requested for limits reconfiguration or disablement, please specify:
   1. CRN string: ...
   1. Which limits to set or disable: For limits to set, provide a requested limit value.
        - [ ] `rate_limit`:
            - [ ] Set value to <...>/second.
            - [ ] Enable with the default value.
            - [ ] Disable.
        - [ ] `max_output_tokens`:
            - [ ] Set value to <...> tokens.
            - [ ] Enable with the default value.
            - [ ] Disable.
        - [ ] `max_input_tokens`:
            - [ ] Set value to <...> tokens.
            - [ ] Enable with the default value.
            - [ ] Disable.
        - [ ] `call_time`:
            - [ ] Set value to <...> seconds.
            - [ ] Enable with the default value.
            - [ ] Disable.
        - [ ] `token_quota`:
            - [ ] Enable.
            - [ ] Disable.

### Request processing (to be completed by the watsonx.ai team)

1. [ ] Send the request for approval.
1. [ ] Prepare PRs for the requested changes in the relevant environments.
1. [ ] Add the PRs to the relevant CR issues.
1. [ ] Inform the requester of the target dates for the changes to be deployed to prod.
1. [ ] Close the ticket when the changes have been deployed.

CC: @otucker @aronovic
