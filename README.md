# ml-planning

Repository used by the Watson Machine Learning team for tracking & planning

# Roadmap and Requirements
The Machine Learning roadmap is defined on an Aha board and synchronised with a Machine Learning requirements Zenhub board both of which are maintained by Offering Management.

[Aha Roadmap] (https://bigblue.aha.io/products/ML/feature_cards)


[Machine Learning Requirements] (https://github.ibm.com/dap/WML-requirements#boards?repos=138899)

# Pre-req
Please install the Zen-hub plug in required to view our Kanban boards and other features.  Download the plug in for either Chrome or Firefox [here](https://zenhub.innovate.ibm.com/setup/download)

# Team Squads

| Squad Name | Squad Scope | Squad Members | Squad Documentation | Hill Info | Kanban View | Slack Channel |
| -------- | ---------- | ------------- | ----------------- |----------------- | --- | ------------- |
| Pipeline | Provide the integrated ML experience for model development and training including HPO,Cross Validation, Experiments, data split, auto feature engineering CADS (auto modeling). Functionality delivered in Spark and additional pipelines like scikit learn/conda and streams | Lucian Cioranu (SCRUM Master)|  | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
| Bluemix Service | Provide the BlueMix integration of WML pipelines for both scoring and training. Focusing on app developer persona and rapid integration int applications | Barbara (SCRUM Master) |  | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline) | |
| Deployment | This service will provide capabilities including Retraining the Model and Monitoring the model performance leading to continuous Model feedback | Barbara (SCRUM Master)| | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
| Scoring | Provides end point capabilities to score ML artifacts in Batch, Streaming and Online modes. | Vinod (SCRUM Master)|  | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
| Ingest and Transform | Provides infrastructure for ingesting into the platform pipelines and into spark. This is the part where WDP executes data profiling and type inference as well as any preprocessing that help data cleansing for DS and ML experience | Janakiraman Krishnamurthy (SCRUM Master)| | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
| Microservices (Common) | Provide the microservice infrastructure using AKKA framework on top of programatic experience and libraries. These are integrated into Canvas and other entry points providing a seamless experience for all usecases. Common Services include capabilities for Scheduling, Repo, Token Service, Security, Framework etc | Janakiraman Krishnamurthy (SCRUM Master)|   | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
| Programmatic Bindings | All the functionality in the platform can also be used from within notebooks. majority of the functional libraries like sparkilng data pipelines etc. have default SCALA bindings. This team is extending the Scala bindings to other programming languages; primarily Python and R | Janakiraman Krishnamurthy (SCRUM Master)|  | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
| Model Visualization | Provide introspection into models and explain plans on execution and decision making. Critical for gaining TRUST on models within organization. Critical part of monitoring for WML | Todd Peterson (SCRUM Master)|  | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
| Canvas |  ML Canvas to allow building and running analytics pipelines and training ML models | Dominika Oliver (SCRUM Master)|  | | [Kanban](https://github.ibm.com/NGP-TWC/ml-planning#boards?labels=WML-pipeline)| |
