---
name: WML BYOM service onboarding request
about: This template should be used to request to onboard with `watsonx.ai` BYOM
title: 'watsonx.ai onboarding request for ...'
labels: WML-BYOM,watsonx,watsonx-inference-proxy,watsonx-fm-dev,devOps,watsonx-byom,watsonx-byom-request
assignees: otucker julianpayne

---

## `watsonx.ai` BYOM onboarding request on public cloud

1. The service name: ...
1. The management approval:
   - [ ] PM: Demi Ajayi @Demi-Ajayi
   - [ ] Dev: Oronde Tucker @otucker
1. The hidden model name:
   1. name: ... (something like `ibm/granite-20b-code-base-v1`) (note that these models need to be deployed to the GPU cluster separately)
   1. DCT #: ...
1. The APIs being used: (select only those that you require)
    - [ ] text/generation (generation/text)
    - [ ] text/generation_stream (generation/text_stream)
1. The service ids per environment: (these service ids must be members of your spaces, see below for how to create a space)
    - QA (staging/yp-qa): ?
    - Prod (us-south): ?
    - Prod (eu-de): ?
1. Is payload logging (OpenScale integration) required: _yes/no_ (if not sure put `no`)
1. Usage estimates? As limits are applied per WML instance usage estimates are required to verify that the
   integration will not hit the limits (under normal usage).
1. Your target date for delivery to production: _dd MMM yyyy_
   Notes:
      1. This should be an estimate, in reality this will depend on the `watsonx.ai` schedule as well as Cloud freezes etc.
      1. The service requesting this model is responsible for all testing (in `yp-qa` and `prod`) so ensure that adequate time is left for testing and any necessary updates in cloud (updates happen at a weekly cadence).
      1. The `watsonx.ai` team will provide a scheduled date once the effort has been sized.

## Checklist for production release

### QA checklist `yp-qa`

**watsonx.ai team:**

- [ ] Model deployed by devops
- [ ] Model added to the models list
- [ ] Service ids added to the secret
- [ ] Inference changes deployed

**IBM product team:**

- [ ] Flow using the service_id tested on `yp-qa`
- [ ] Performance testing done on `yp-qa` (within the resource constraints in `yp-qa`)

### Production checklist

**watsonx.ai team:**

- [ ] Model deployed by devops
- [ ] Model added to the models list
- [ ] Service ids added to the secret
- [ ] Inference changes deployed

**IBM product team:**

- [ ] Flow using the service_id tested on `prod`
- [ ] Performance testing done on `prod`

**Notes:**

1. If you have the `user_id` of the user requesting the call you can also pass it in the `X-WML-User-Id` HTTP header.
1. `QA` cluster -> `yp-qa` <https://yp-qa.ml.cloud.ibm.com/>

## Creating a space or project for testing

The easiest way to create a space or project is to login to the `watsonx` UI with the same user as the `service_id`
and create the space or project using the UI.

1. `QA` -> <https://dataplatform.test.cloud.ibm.com/login?context=wx>
1. `Prod` -> <https://dataplatform.cloud.ibm.com/login?context=wx> (choose the region)

If you want to create the space or project by API you can find the API docs here:

1. `Spaces` -> <https://pages.github.ibm.com/AILifecycle/cpd-spaces-api/>
1. `Projects` -> <https://api.dataplatform.cloud.ibm.com/v2/projects/docs/swagger/>

The mapping for the environments is the same as for the UI:

1. `QA` -> <https://dataplatform.test.cloud.ibm.com/>
1. `Prod` -> <https://dataplatform.cloud.ibm.com/>

Cc: @otucker @julianpayne
