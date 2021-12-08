---
name: WML remove runtime definition
about: This template should be used to track the work for a removing WML runtime
title: ''
labels: wml
assignees: ''

---

# WML checklist for delivering new runtime definition

 - [ ] OM: provide deprecation announcement date
 - [ ] V4Repo-service: deprecate model types, coordinate with deprecation announcement date  @siucht
 - [ ] UI: provide deprecation warning @chrisj
 - [ ] OM: provide removal date, it should be coordinated with weekly CR
 - [ ] Environment: remove software spec, coordinated with removal date @alexlang 
 - [ ] V4Repo-service: remove model types, coordinated with removal date  @siucht
 - [ ] Training-service: remove from list of supported runtime definition @kamilabaron-palucka
 - [ ] WS Notebook team: [TBD add task if needed]
 - [ ] Deployment service: @nrabakav
 - [ ] UI: remove runtime @chrisj
 - [ ] Documentation: update WML docs @julianne-forgo
 - [ ] QA: @dennis-windsor 
