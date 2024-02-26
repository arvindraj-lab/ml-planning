---
name: Watsonx.ai model benchmarking
about: This template should be used to track model quality benchmarking from perspective of prompt engineering/tuning
title: 'Benchmarking and rating of <model_name> - prompt <engineering/tuning>'
labels: watsonx-FM-eval,watsonx.ai,task
assignees: daniel-ryszka,Lukasz-Cmielowski
---

## Benchmarking and rating of <model_name> - prompt <engineering/tuning>
- [ ] run benchmarks on:
  - [ ] WML
  - [ ] BAM (only if there are blockers/issues with WML)
- [ ] open defects:
  - [ ] in ml-planning if you encounter any issues with models (WML/watsonx.ai)
  - [ ] in fm-eval if you encounter any issues with benchmarking tool
- [ ] paste results (charts) of benchmarking with comparison to other models (wherever possible)
- [ ] prepare list of supported tasks and ratings per task for FM Dev team (add @Lukasz-Cmielowski as reviewer)
- [ ] prepare list of proposed new default values (if different than current) of parameters for FM Dev team (add @Lukasz-Cmielowski as reviewer)
- [ ] after review, tag issue with `watsonx-fm-dev` label/team
- [ ] get/prepare sample prompt
- [ ] prepare sample notebook
