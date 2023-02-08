---
name: 'Spaces Asset Onboarding '
about: 'General template for onboarding new asset type to Spaces. '
title: Spaces Onboarding for <New Asset Type>
labels: WML-UI
assignees: chrisj, nickmazz, ychien

---

- [ ] Create or update Asset Extension Registry metadata
  - If you do not already have an asset extension for the projects container, create a new `your_asset_type` asset extension. For reference:
    - https://pages.github.ibm.com/data-platform/asset-extension-registry/getting-started
  - Create a `your_asset_type.space.json` file in your asset extension folder and add the following logic to `your_asset_type.js` file. For reference:
    - [Notebook asset js](https://github.ibm.com/data-platform/asset-extension-registry/blob/master/extensions/notebook/notebook.js#L42) (Logic to return the space json data in a space container)
    - [Notebook asset space json](https://github.ibm.com/data-platform/asset-extension-registry/blob/master/extensions/notebook/notebook.space.json) (Defines actions and columns specific to the space context)
    - [Notebook asset projects json](https://github.ibm.com/data-platform/asset-extension-registry/blob/master/extensions/notebook/notebook.json) (Defines general asset metadata such as name, description, and owner. Values for keys that are also defined in the `.space.json` file will be overridden by the space values)


- [ ] update portal-job-manager with new asset type (if export / import support required), for reference:
  - https://github.ibm.com/dap/portal-job-manager/pull/140/files
  - https://github.ibm.com/dap/portal-job-manager/pull/143/files

- [ ] update wml-main promotion handling (if custom promotion logic required), for reference:
  - https://github.ibm.com/WML/wml-main/blob/master/controllers/_api/catalogs-api-controller.js#L1178
  - Current state of promotion wrapper API -- https://github.ibm.com/NGP-TWC/ml-planning/issues/30142

- [ ] update supported asset type list for export / import in wml-main, for reference:
  - https://github.ibm.com/WML/wml-main/blob/master/src/routes/components/Space/routes/components/SpaceImportSummary/SpaceImportSummary.js#L84

- [x] communicate to Spaces API team for awareness, FYI @ rafal-bigaj @ Kamil-Huras1

- [x] communicate to Spaces design team for awareness, FYI @thollifi @liw

- [x] communicate to Spaces QA team for awareness, FYI @elainep @Dennis-Windsor
