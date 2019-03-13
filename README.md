# ml-planning

Repository used by the Watson Machine Learning team for tracking & planning

# Roadmap and Requirements
The Machine Learning roadmap is defined on an Aha board maintained by Offering Management.

[Aha Roadmap](https://bigblue.aha.io/products/ML/feature_cards)

[Aha Epics on Planning board](https://github.ibm.com/NGP-TWC/ml-planning/issues/6417#workspaces/582b95f47d2715684be61191/boards?labels=aha!%3Ain%20development,aha!%3Anew,aha!%3Aready%20for%20development,aha!%3Aunder%20consideration,aha!ready%20for%20design&filterLogic=any&useDefaultFilterLogic=false&repos=84379)

[Box Folder](https://ibm.ent.box.com/folder/21779425598)


# Pre-req
Please install the Zen-hub plug in required to view our Kanban boards and other features.  Download the plug in for either Chrome or Firefox [here](https://zenhub.innovate.ibm.com/setup/download)

# Squads

| Squad Name | Squad Scope | Mgmt Contact | Squad Members |
| ---------- | ----------- | ------------ | -------------------- |
| Training | Provide the integrated ML experience for model development and training including HPO, Cross Validation, Experiments, data split, auto feature engineering CADS (auto modeling). Functionality delivered in Spark and additional pipelines like scikit learn/conda and streams | Lucian Cioranu | **Lucian Cioranu (Lead)**, Calin Cocan, Mihai Sarto |
| Deployment & Scoring | This squad develop the core framework and capabilities to Deploy and Score models in Online, Batch and Streaming modes. This squad also handle the support for runtimes like Spark, PMML and SPSS. A sub squad also handle Python and DL frameworks like ScikitLearn, XGBoost, Tensorflow, Keras, Caffe and upcoming PyTorch  | Vinod Khader | **Tamilselvan Narayanaswamy (Lead)**, Dinoop Thomas, Venkateshwara S Goutham, Rajyalakshmi Nandireddy, Srijak Bhaumik1, Niveditha Rabakavi, Kavya J Rao,  **Krishnamurthy Arthanarisamy (Python RT Lead)**, Srikrishna S Bhat, Ginbiaksang Naulak  | 
| Learning-Systems | This service will provide capabilities including Retraining the Model and Monitoring the model performance leading to continuous Model feedback | Vincent Beraudier | **Vincent Beraudier (Lead)**, Julian Payne, Aurelie Folacci |
| Repository | This service manages all the CRUD operations w.r.t WML resources( Spaces, Models, Experiments, Pipelines, Functions, Runtimes, Libraries )  | Janakiraman Krishnamurthy | **Mithun Virajpet (Lead), Roopa Mahendra (Lead)**, Mahadev Khapali, Sobha Rani Cheruku, Kayalvizhi Ganesan |
| Ingest | This service handles the Connectors and Data ingest capabilities during Training cycle  | Janakiraman Krishnamurthy | Yugandhra Rayanki/India/IBM |
| Token | This service manages tokens that are used by users and all other services  | Janakiraman Krishnamurthy | Kayalvizhi Ganesan
| DevOps | Continuous Integration, Automation, Overall operation across Data Centers and Private cloud  | Janakiraman Krishnamurthy | **Shashank Vagarali (Lead)**, Prabhu S Padashetty, Estee J Mathew, Jins M Alex, Hemant K Singh | 
| Cloud Broker | Service broker for Cloud integration  | Vinod Khader | **Shashank Vagarali**, Hemant K Singh| 
| Reporting | This service manages all events and reporting metrics  | Vinod Khader | **Shashank Vagarali (Lead)**, Sahana Ha Anantharajaiah | 
| Instances | This service manages WML instance operations on Cloud  | Vinod Khader | **Shashank Vagarali (Lead)**, Sahana Ha Anantharajaiah | 
| Client library | Python Library to leverage WML capabilities from Notebooks  | Vinod Khader | **Shashank Vagarali (Lead)**, Hanisha Nagireddy, Kamini Gupta | 
| CLI | Command line interface for WML | Vinod Khader | **Shashank Vagarali (Lead)**, Hanisha Nagireddy, Kamini Gupta | 
| DL | Deep Learning Service that powers Training for DL frameworks  | Oronde Tucker | **Paul Van Run (architect)**, David Tam, Jim Rhyness, Cong Lin| 
| Model Visualization | Provide introspection into models and explain plans on execution and decision making. Critical for gaining TRUST on models within organization. Critical part of monitoring for WML  | Todd Peterson | |
| Modeler Flows |  ML Canvas to allow building and running analytics pipelines and training ML models  | Darren Sullivan |  |
| Neural Network editor | Part of the Modeler Flows experience, the Deep Learning Editor(AKA Darviz) allows users to visually create a Neural Network definition which can be saved to the ML Repository for Training withing the service  | Yawen Chien |  |

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
- Public apis: http://watson-ml-api.mybluemix.net
- Current draft of v4 public apis: http://watson-ml-v4-api.mybluemix.net
- Current draft of v4 private apis: http://watson-ml-v4-api-private.mybluemix.net
- Private v3 API - http://watson-ml-v3-api-private.mybluemix.net
- Private v2 API - http://watson-ml-v2-api-private.mybluemix.net

### APIs promotion path
- design-api -> private - > public
- design-api-private -> private

# Important Slack channels
- #wml-dev - For all development queries
- #wml-pd-ops - For all Production issues and outages
- #wml-user - For all WML users to raise questions, issues etc
- #wml-on-icp - For discussions on WML on ICP4D
