---
name: Watsonx.ai BYOM service onboarding request
about: This template should be used to request to onboard with `watsonx.ai` BYOM
title: 'watsonx.ai onboarding request for ...'
labels: WML-BYOM,watsonx,watsonx-inference-proxy,watsonx-fm-dev,devOps,watsonx-byom,watsonx-byom-request
assignees: otucker,julianpayne,Demi-Ajayi,aronovic,tamdavid

---

## `watsonx.ai` BYOM onboarding request on public cloud

1. The service name: ...
1. The management approval:
   - [ ] PM: Demi Ajayi @Demi-Ajayi
   - [ ] Dev: Oronde Tucker @otucker
1. The custom model name:
   1. name: ... (something like `ibm/granite-20b-code-base-v1`) (note that these models need to be deployed to the GPU cluster separately)
   1. DCT #: ...
1. The APIs being used: (select only those that you require)
    - [ ] text/generation (generation/text)
    - [ ] text/generation_stream (generation/text_stream)
1. The service ids per environment: (these service ids must be members of your spaces, see below for how to create a space)
    - Prod (us-south): ...
    - Prod (eu-de): ...
    - Prod (jp-tok): ...
1. Is payload logging (OpenScale integration) required: _yes/no_ (if not sure put `no`)
1. Usage estimates? As limits are applied per WML instance usage estimates are required to verify that the
   integration will not hit the limits (under normal usage).
1. Your target date for delivery to production: _dd MMM yyyy_
   Notes:
      1. This should be an estimate, in reality this will depend on the `watsonx.ai` schedule as well as Cloud freezes etc.
      1. The service requesting this model is responsible for all testing (in `prod`) so ensure that adequate time is left for testing and any necessary updates in cloud (updates happen at a weekly cadence).
      1. The `watsonx.ai` team will provide a scheduled date once the effort has been sized.

## Checklist for production release

### Production checklist

**watsonx.ai team:**

- [ ] Model deployed by devops to production (whichever clusters were requested)
- [ ] Model added to the models DB and consumer added to consumers DB
- [ ] Service ids added to the secret
- [ ] Inference changes deployed

**IBM product team:**

- [ ] Flow using the service_id tested on `prod`
- [ ] Performance testing done on `prod`

**Notes:**

1. If you have the `user_id` of the user requesting the call you can also pass it in the `X-WML-User-Id` HTTP header.

## Creating service_ids for production

The account owner, i.e. the account that is going to pay (depending on finance arrangements) for this use,
needs to create a service_id for each environment (prod-us-south, prod-eu-de, etc) and then use the same
account to create the space or project as described below.

Creation of a service_id is done by going to the following consoles via the `Access (IAM)` menu in the left hand pane:

1. `Prod` -> <https://dataplatform.cloud.ibm.com/login?context=wx>

## Creating a space or project for testing

The easiest way to create a space or project is to login to the `watsonx` UI with the same user as the `service_id`
and create the space or project using the UI. Once the space or project is created then the service_id needs to be
added as a member.

1. `Prod` -> <https://dataplatform.cloud.ibm.com/login?context=wx> (choose the region)

If you want to create the space or project by API you can find the API docs here:

1. `Spaces` -> <https://cloud.ibm.com/apidocs/watson-data-api#spaces-create>
1. `Projects` -> <https://cloud.ibm.com/apidocs/watson-data-api#projects-list>

The mapping for the environments is the same as for the UI:

1. `Prod` -> <https://dataplatform.cloud.ibm.com/>
