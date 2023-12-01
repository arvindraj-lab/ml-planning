---
name: Watsonx.ai limits change request
about: This template should be used to request a change in the `watsonx.ai` limits for specific instance IDs
title: 'watsonx.ai limits change request'
labels: watsonx-limits-change-request,watsonx-fm-dev,watsonx-inference-proxy,watsonx
assignees: aronovic,otucker
---

## Request to change `watsonx.ai` limits for instance IDs in public cloud

### Request details (to be completed by the requester)

#### Background

It is possible to reconfigure or disable the following limits for an instance ID:

- `rate_limit`: This limit is specified in terms of the maximum number of requests per second for the instance ID.

#### Request

To reconfigure or disable specific limits for specified instance IDs, please provide the following information:

1. Name of customer / product: ...
1. Background / reason for the request: ...
1. Links to associated tickets: ...
1. For IBM teams embedding watsonx.ai for product or project use:  
   - [ ] An [embed intake form](https://github.ibm.com/NGP-TWC/ml-planning/issues/new?assignees=Demi-Ajayi&labels=watsonx%2Cembed&template=watsonx-embed-intake.md&title=watsonx.ai+embed+intake+form+for+%5Bproduct+name+%2B+feature%5D) has been submitted, and the requester is following the [watsonx.ai process](https://w3.ibm.com/w3publisher/using-llms-ibm/delivery-playbook).
1. Requested date for applying the change:
   - [ ] As soon as possible.
   - [ ] Date: ...
1. Requested date for removing the change:
   - [ ] Indefinite.
   - [ ] Date: ...
1. For each CRN that is requested for limits reconfiguration or disablement, please specify:
   1. CRN string: ...
   1. The limits to set or disable:
        - `rate_limit`:
            - [ ] Set value to <...>/second.
            - [ ] Enable with the default value.
            - [ ] Disable.

### Request processing (to be completed by the watsonx.ai team)

1. [ ] Send the request for approval.
1. [ ] Prepare PRs for the requested changes in the relevant environments.
1. [ ] Add the PRs to the relevant CR issues.
1. [ ] Inform the requester of the target dates for the changes to be deployed to prod.
1. [ ] Close the ticket when the changes have been deployed.

CC: @otucker @aronovic @julianpayne @Demi-Ajayi
