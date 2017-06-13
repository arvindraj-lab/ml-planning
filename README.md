# ml-planning

Repository used by the Watson Machine Learning team for tracking & planning

# Roadmap and Requirements
The Machine Learning roadmap is defined on an Aha board and synchronised with a Machine Learning requirements Zenhub board both of which are maintained by Offering Management.

[Aha Roadmap](https://bigblue.aha.io/products/ML/feature_cards)

[Requirements Board](https://github.ibm.com/dap/WML-requirements#boards?repos=138899)

[Box Folder](https://ibm.ent.box.com/folder/21779425598)

# Pre-req
Please install the Zen-hub plug in required to view our Kanban boards and other features.  Download the plug in for either Chrome or Firefox [here](https://zenhub.innovate.ibm.com/setup/download)

# Team Squads

| Squad Name | Squad Scope | Squad Leader | Reporting |
| -------- | ---------- | ------------- | -------- |
| Training | Provide the integrated ML experience for model development and training including HPO,Cross Validation, Experiments, data split, auto feature engineering CADS (auto modeling). Functionality delivered in Spark and additional pipelines like scikit learn/conda and streams | Lucian Cioranu | Anthony Casaletto |
| Bluemix Service | Provide the BlueMix integration of WML pipelines for both scoring and training. Focusing on app developer persona and rapid integration int applications | Kamila Baron-Palucka | Anthony Casaletto |
| Deployment | This service will provide capabilities including Retraining the Model and Monitoring the model performance leading to continuous Model feedback | Rafal Bigaj | Anthony Casaletto |
| Scoring | Provides end point capabilities to score ML artifacts in Batch, Streaming and Online modes. | Tamil Narayanaswamy | Vinod Khader |
| Core services | Ingest Integration, Repo, Token, Libraries, Run time Integration (Scikit learn) | Janakiraman Krishnamurthy | Vinod Khader |
| Continuous Integration | Continuous Integration, Automation | Shashank Vagarali| Vinod Khader |
| Model Visualization | Provide introspection into models and explain plans on execution and decision making. Critical for gaining TRUST on models within organization. Critical part of monitoring for WML | Todd Peterson | Anthony Casaletto |
| Canvas |  ML Canvas to allow building and running analytics pipelines and training ML models | Dominika Oliver | Anthony Casaletto |
| Deep Learning | Deep Learning as a Service | Florian Rosenberg | Rania Khalaf |

# Guilds

A Guild is a group of people that form a community of interest across the full organization to share knowledge, tools, code, and practices.

| Guild Name | Scope | Leader | Reporting | Members |
| -------- | ---------- | ------------- | -------- | -------- |
| Architecture | Drive Architecture direction across WML | Marius Danciu| Anthony Casaletto | Marius Danciu, Gopi Varadarajulu, Rafal Bigaj, Florian Rosenberg, Robert Duncan, Donald Pierucci |
| Performance | Drive Performance Strategy across WML | Basker Shanmugam| Vinod Khader | Basker Shanmugam, Lukasz Cmielowski, Andrew Thompson |
| Metrics | Drive Metric collection and reporting | Rafal Bigaj | Vinod Khader | Rafal Bigaj, Shashank Vagarali, Andrew Thompson |
| QA | Drive Test strategy across WML | Lukasz Cmielowski | Anthony Casaletto | Lukasz Cmielowski, Andrew Thompson, Diana Tesedean, Yugandhra Rayanki |
| Operations | Drive Operations strategy across WML including Continuous Integration, Runbooks | Shashank Vagarali | Vinod Khader | Shashank Vagarali, Daniel Ryszka, Mihai Sarto, Andrew Thompson  |
| Security | Security reviews and strategy across WML | Rafal Bigaj | Anthony Casaletto | Rafal Bigaj, Gopi Varadarajulu |
| NFR | NFR reviews and strategy across WML | Gopi Varadarajulu | Vinod Khader | Gopi Varadarajulu |

## Making guilds effective
There are a set of principles that each guild needs to folow up.

1. Guilds typically discuss in more depth technical aspects, of their domain, that are generally applicable to all squads. However guilds need to clearly forumulate the outcomes of that effort and make concrete proposals before implementing them. 

2. Technical proposals of different guilds needs to be communicated to the Architecure guild. Use wml-architecture slack channel to make such communications.

3. There is a need for cross-guild communication. For instance security guild may need something implemented but that may affect performance thus involving the performance and architecture guilds is recommended. 

