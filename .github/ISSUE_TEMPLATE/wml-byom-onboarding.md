---
name: WML BYOM service onboarding request
about: This template should be used to request to onboard with `watsonx.ai` BYOM
title: 'watsonx.ai BYOM onboarding request'
labels: WML-BYOM,watsonx,watsonx-inference-proxy,watsonx-fm-dev,devOps,watsonx-byom
assignees: julianpayne

---

## `watsonx.ai` BYOM onboarding request on public cloud

1. The service name: ...
1. The hidden model name: ... (something like `ibm/granite-20b-code-base-v1`)
1. The APIs being used: (select only those that you require)
    - [ ] text/generation
    - [ ] text/generation_stream
1. The service ids per environment: (these service ids must be members of your spaces)
    - Dev: ?
    - QA (staging): ?
    - Prod (us-south): ?
    - Prod (eu-de): ?
1. Is payload logging (OpenScale integration) required: yes/no (if not sure put `no`)
1. Usage estimates? As limits are applied per WML instance usage estimates are required to verify that the
   integration will not hit the limits (under normal usage).

**Notes:**

1. If you have the `user_id` of the user requesting the call you can also pass it in the `X-WML-User-Id` HTTP header.
1. `Dev` -> `fvt` and `ys1prod` clusters.
1. `QA` -> `yp-qa` and `yp-cr` clusters.
