---
name: 'Spaces Asset Onboarding '
about: 'General template for onboarding new asset type to Spaces. '
title: Spaces Onboarding for <New Asset Type>
labels: WML-UI
assignees: chrisj, ychien, nickmazz

---

- [ ] create / update Asset Extension Registry metadata, for reference:
  - https://github.ibm.com/data-platform/asset-extension-registry/blob/master/extensions/notebook/notebook.space.json

- [ ] update portal-job-manager with new asset type (if export / import support required), for reference:
  - https://github.ibm.com/dap/portal-job-manager/pull/140/files
  - https://github.ibm.com/dap/portal-job-manager/pull/143/files

- [ ] update wml-main promotion handling (if custom promotion logic required), for reference:
  - https://github.ibm.com/WML/wml-main/blob/master/controllers/_api/catalogs-api-controller.js#L1178
  - Current state of promotion wrapper API -- https://github.ibm.com/NGP-TWC/ml-planning/issues/30142

- [ ] update supported asset type list for export / import in wml-main, for reference:
  - https://github.ibm.com/WML/wml-main/blob/master/src/routes/components/Space/routes/components/SpaceImportSummary/SpaceImportSummary.js#L84

- [ ] communicate to Spaces API team for awareness, FYI @ rafal-bigaj @ Kamil-Huras1
