# ml-planning

Repository used by the Watson Machine Learning team for tracking & planning

# Roadmap and Requirements
The Machine Learning roadmap is defined on an Aha board maintained by Offering Management.

[Aha Roadmap](https://bigblue.aha.io/products/ML/feature_cards)

[Box Folder](https://ibm.ent.box.com/folder/21779425598)


# Pre-req
Please install the Zen-hub plug in required to view our Kanban boards and other features.  Download the plug in for either Chrome or Firefox [here](https://zenhub.innovate.ibm.com/setup/download)

# Squads

| Squad Name | Squad Scope | Mgmt Contact | Squad Lead & Members |
| ---------- | ----------- | ------------ | -------------------- |
| Training | Provide the integrated ML experience for model development and training including HPO, Cross Validation, Experiments, data split, auto feature engineering CADS (auto modeling). Functionality delivered in Spark and additional pipelines like scikit learn/conda and streams | Lucian Cioranu/Romania/IBM | Lucian Cioranu/Romania/IBM (Lead), Calin Cocan/Romania/IBM, Mihai Sarto/Romania/IBM |
| Deployment & Scoring | This service will provide capabilities to Deploy and Score models | Vinod Khader/India/IBM | Tamilselvan Narayanaswamy (Lead)
AAA | 
| Learning-Systems | This service will provide capabilities including Retraining the Model and Monitoring the model performance leading to continuous Model feedback | Mithun Virajpet | 
| Repository | This service manages the APIs to save and load all ML artifacts including Models | | Janakiraman Krishnamurthy | 
| Ingest | This service handles the Connectors and Data ingest capabilities during Training cycle  | | Janakiraman Krishnamurthy | 
| Token | This service manages tokens that are used by users and all other services  | | Janakiraman Krishnamurthy | 
| DevOps | Continuous Integration, Automation, Overall operation across Data Centers and Private cloud  | | Shashank Vagarali| 
| Cloud Broker | Service broker for Cloud integration  | Vinod Khader/India/IBM | Shashank Vagarali|
| Events | This service manages all events and reporting metrics  | Vinod Khader/India/IBM | Shashank Vagarali| 
| Instances | This service manages WML instance operations on Cloud  | Vinod Khader/India/IBM | Shashank Vagarali| 
| Client library | Python Library to leverage WML capabilities from Notebooks  | Vinod Khader/India/IBM | Shashank Vagarali| 
| CLI | Command line interface for WML | Vinod Khader/India/IBM | Shashank Vagarali| 
| DL | Deep Learning Service that powers Training for DL frameworks  | | Oronde Tucker| 
| Model Visualization | Provide introspection into models and explain plans on execution and decision making. Critical for gaining TRUST on models within organization. Critical part of monitoring for WML  | | Todd Peterson |
| Modeler Flows |  ML Canvas to allow building and running analytics pipelines and training ML models  | | Darren Sullivan | 
| Neural Network editor | Part of the Modeler Flows experience, the Deep Learning Editor(AKA Darviz) allows users to visually create a Neural Network definition which can be saved to the ML Repository for Training withing the service  | | Yawen Chien | 

# Guilds

A Guild is a group of people that form a community of interest across the full organization to share knowledge, tools, code, and practices.

| Guild Name | Scope | Leader | Reporting | Members |
| -------- | ---------- | ------------- | -------- | -------- |
| Architecture | Drive Architecture direction across WML | Marius Danciu| Anthony Casaletto | Marius Danciu, Robert Duncan, Donald Pierucci |
| Performance | Drive Performance Strategy across WML | Basker Shanmugam| Vinod Khader | Basker Shanmugam, Andrew Thompson |
| Metrics | Drive Metric collection and reporting | Shashank Vagarali | Vinod Khader | Shashank Vagarali, Andrew Thompson |
| QA | Drive Test strategy across WML | Monica Romila | Remus Lazar | Monica Romila, Diana Tesedean, Elaine, Nikhil, Nareen |
| Operations | Drive Operations strategy across WML including Continuous Integration, Runbooks | Shashank Vagarali | Vinod Khader | Shashank Vagarali, Prabhu S Padashetty, Estee J Mathew, Jins M Alex, Hemant K Singh, Mihai Sarto, Andrew Thompson  |
| Security | Security reviews and strategy across WML | TBD | Anthony Casaletto | TBD |
| Compliance | Compliance execution across WML | Janakiraman Krishnamurthy | Vinod Khader | Janakiraman Krishnamurthy, Devops squad |

## Making guilds effective
There are a set of principles that each guild needs to folow up.

1. Guilds typically discuss in more depth technical aspects, of their domain, that are generally applicable to all squads. However guilds need to clearly forumulate the outcomes of that effort and make concrete proposals before implementing them. 

2. Technical proposals of different guilds needs to be communicated to the Architecure guild. Use wml-architecture slack channel to make such communications.

3. There is a need for cross-guild communication. For instance security guild may need something implemented but that may affect performance thus involving the performance and architecture guilds is recommended. 

# WML clusters

- FVT: wml-fvt.ml.test.cloud.ibm.com
- DEV: wml-dev.ml.test.cloud.ibm.com
- SVT: wml-svt.ml.test.cloud.ibm.com
- PERF: wml-perf.ml.test.cloud.ibm.com
- YS1-PROD: us-south.ml.test.cloud.ibm.com
- LYS1-PROD: eu-gb.ml.test.cloud.ibm.com
- YP-PROD: us-south.ml.cloud.ibm.com
- LYP-PROD: eu-gb.ml.cloud.ibm.com


# Swagger pages
- Implemented public v3 API - http://watson-ml-v3-api.mybluemix.net
- Implemented private v3 API - http://watson-ml-v3-api-private.mybluemix.net
- Implemented private v2 API - http://watson-ml-v2-api-private.mybluemix.net
- APIs in design that will eventually become public - http://watson-ml-design-api.mybluemix.net
- APIs in desgin for private use only - http://watson-ml-design-api-private.mybluemix.net

### APIs promotion path
- design-api -> private - > public
- design-api-private -> private
