---
name: WML deprecate/remove software specification on Cloud
about: This template should be used to track the work for a deprecating/removing WML sw-specification
title: ''
labels: wml
assignees: ''

---

# WML checklist for deprecating

 - [ ] OM: provide dates for deprecation, blocking creating new trainings/models, and removal of the sw-spec
 - [ ] V4Repo: mark sw-spec and corresponding model_types as deprecated/create-unsupported/unsupported with coordination to deprecation dates  @siucht
 - [ ] Training-service: remove from list of supported runtime definition (if applicable) @kamilabaron-palucka
 - [ ] Training-service: remove taining templates (if applicable) @kamilabaron-palucka
 - [ ] UI: provide appropriate messages depending on sw-spec state @chrisj
 - [ ] WS Notebook team: [TBD add task if needed]
 - [ ] Deployment service: @nrabakav
 - [ ] Documentation: update WML docs @julianne-forgo
 - [ ] QA: @dennis-windsor 
