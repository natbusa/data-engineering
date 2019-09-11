# Data Engineering

How would you bootstrap a Data Team? Here below a "laundry list" of tasks, resources, job profiles, and blueprints on how to build a dream data team. Mission: manage all the data, learn from it, and deliver concrete and tangible business results to the rest of the organization.

## Team

Profiles share both a Dev and Production Load.
 - 1x [Infra](profiles/infra.md) (Metal, Physical, Metal as a service, IaaS)
 - 1x [DevOps](profiles/devops.md) (Stack automation,, Containers and Platform as a service)
 - 2x [Data Engineer](profiles/data.md) (Data Pipelines, Data Automation, Data as a Service, Data Ingestion)
 - 2x [Analytics](profiles/analytics.md) (1x Batch Analytics, 1x Real-Time Analytics and Predictive APIs)
 - 1x [AI and ML](profiles/ai.md) (Machine Learning and AI algorithms)
 - 1x [Front-End Dev](profiles/frontend.md) (Web and Js developer, web and mobile apps)

Extended team: for small scale projects, above profiles can cover the  extended team's tasks:

 - 1x Network Architect
 - 1x Security Engineer
 - 1x Community Writer
 - 1x Data Viz Developer

### Getting started team
Read, learn, memorize and *practice* the following:
 - python
   - https://docs.python.org/3/tutorial/
   - https://docs.python.org/3/library/
   - https://docs.python.org/3/reference/datamodel.html

 - bash commands and Makefile:
   - http://oliverelliott.org/article/computing/ref_unix/
   - https://www.gnu.org/software/make/manual/make.html

 - spark:  
 from http://spark.apache.org/docs/latest/sql-programming-guide.html
   - http://spark.apache.org/docs/latest/sql-data-sources-avro.html
   - http://spark.apache.org/docs/latest/sql-data-sources-hive-tables.html
   - http://spark.apache.org/docs/latest/sql-data-sources-jdbc.html
   - http://spark.apache.org/docs/latest/sql-data-sources-json.html
   - http://spark.apache.org/docs/latest/sql-data-sources-load-save-functions.html
   - http://spark.apache.org/docs/latest/sql-data-sources-orc.html
   - http://spark.apache.org/docs/latest/sql-data-sources-parquet.html
   - http://spark.apache.org/docs/latest/sql-data-sources-troubleshooting.html
   - http://spark.apache.org/docs/latest/sql-data-sources.html
   - http://spark.apache.org/docs/latest/sql-distributed-sql-engine.html
   - http://spark.apache.org/docs/latest/sql-getting-started.html
   - http://spark.apache.org/docs/latest/sql-migration-guide-hive-compatibility.html
   - http://spark.apache.org/docs/latest/sql-migration-guide-upgrade.html
   - http://spark.apache.org/docs/latest/sql-migration-guide.html
   - http://spark.apache.org/docs/latest/sql-performance-tuning.html
   - http://spark.apache.org/docs/latest/sql-pyspark-pandas-with-arrow.html
   - http://spark.apache.org/docs/latest/sql-reference.html

from pyspark python documentation:
   - http://spark.apache.org/docs/latest/api/python/pyspark.html
   - http://spark.apache.org/docs/latest/api/python/pyspark.sql.html

## Principles

 - Python is the default language for the data stack.
 - Engineers over Scientists
 - Convention over Configuration over Coding.
 - More thinking less typing
 - Keep it simple
 - Re-use over Integrate over Build.
 - Service Oriented (CLI, Web HTTP APIs , Python Libraries)
 - Be kind, be curious

### Tools Specific Principles
#### Spark
Spark is a library with many cohexisting layers, mostly because of back compatibility some of this APIs are still around both in the tool as well on the web with many Q&A still going round. When learning Spark please follow the following principles:

 - pyspark only (https://spark.apache.org/docs/latest/api/python/)
 - Learn ONLY the modules: pyspark.sql and pyspark.ml
 - Skip anything related to Scala, Java, R (according to the above general principle)
 - Skip categorically anything about RDDs, Map-Reduce, and MLlib

#### Git
Git is meant for people to experiment, develop and merge working code on a common master branch.   
Please follow the given principles.
 - No working branches on the shared remote (gitlab/github) repo
 - Pull requests over commits
 - Diff and Test the code *before* commiting

Best way of working:
 - fork the remote common repository from gitlab/github
 - add multiple remotes to keep track on changes and rebase/marge if necessary
 - commit to your remote and pull request to the main repo.

## Hardware

Storage 2-sockets  
($22.5k, 16C, 256GB, 144TB, 2x10Gb):
  - PowerEdge R740xd (2 sockets, 2U, 12 x 3.5 bays)
  - (2x) Intel® Xeon® Silver 4110 2.1G, 8C/16T, 9.6GT/s, 11M Cache, Turbo, HT (85W) DDR4-2400
  - (8x) 32GB RDIMM, 2666MT/s, Dual Rank
  - (12x) 12TB 7.2K RPM SATA 6Gbps 512e 3.5in Hot-plug Hard Drive
  - Broadcom 57416 2 Port 10Gb Base-T + 5720 2 Port 1Gb Base-T, rNDC

Vanilla 2-sockets  
($23k, 28C, 512GB, 64TB, 2x10Gb):
  - PowerEdge R740xd (2 sockets, 2U, 12 x 3.5 bays)
  - (2x) Intel® Xeon® Gold 5120 2.2G, 14C/28T, 10.4GT/s, 19M Cache, Turbo, HT (105W) DDR4-2400
  - (16x) 32GB RDIMM, 2666MT/s, Dual Rank
  - (8x) 8TB 7.2K RPM NLSAS 12Gbps 512e 3.5in Hot-plug Hard Drive
  - Broadcom 57416 2 Port 10Gb Base-T + 5720 2 Port 1Gb Base-T, rNDC

Compute 4 sockets  
($25k, 40C, 512GB, 9.6TB, 2x10Gb):
  - PowerEdge R830 (4 sockets, 2U, 16 x 2.5”)
  - (4x) Intel® Xeon® E5-4620 v4 2.1GHz,25M Cache,8.0 GT/s,Turbo,HT,10C/20T (105W) DDR4 2133 MHz
  - (16x) 32GB RDIMM, 2400MT/s, Dual Rank, x4 Data Width
  - (4x) 2.4TB 10K RPM SAS 12Gbps 512e 2.5in Hot-plug Hard Drive
  - QLogic 57800 2x10Gb BT + 2x1Gb BT Network Daughter Card

## Resources
 - [data resources](resources.md)
 - [datalabframework](

## Use cases
Refer to [usecases.md](usecases.md) for a more detailed description of the following e-retail and e-commerce use cases.

 -  Recommendation engines
 -  Market basket analysis
 -  Warranty analytics
 -  Price optimization
 -  Inventory management
 -  Customer sentiment analysis
 -  Merchandising
 -  Lifetime value prediction
 -  Fraud detection
 -  Option Selection (A/B testing)
 -  UX automation
 -  Data mining
 -  Chatbots

 ## Architecture

  - Management
    - Versioning: __gitlab__  
    - CI-CD Framework: __gitlab-ci__  
    - Resource Management: __Kubernetes__

  - Storage
    - Storage (Landing Storage): __HDFS__
    - Storage (Object Store): __Minio__
    - Storage (Block Storage): __Ceph__

  - Data Transport
    - Pub/Sub Infrastructure: __Kafka__

  - Data Analytics
    - Indexed data: __Elasticsearch__
    - Ingestion and ETL Framework: __Spark__
    - Data Science: __Pandas/Scikit-Learn__
    - BI Visualization: __Kibana__

  - Data Formats:
     - etl: __parquet__
     - indexes: __elasticsearch__
 	- ds/ml: __hdf5__
 	- cache: __Redis__

 ## Data Architecture



 ### Ingestion Framework

 #### Sources

   - DBs
   - Files
   - Streams

 #### Targets

   - Change Logs
   - Table Snapshots
   - Data Views

 #### Principles and Solutions:

   - Mutable Tables to Immutable Change Logs
   - Idempotency / Repeatability
   - Record Schema Changes
   - Implement validation strategies
   - Automated Data pipelines
   - Implement a Data Access Strategy
   - Define Merge commits behavior
   - Create Commit Robots/Agents
   - Define Promotion Strategy
   - Define a Data Sampling strategy

 #### Monitoring and CI-CD Pipeline:
   - Dashboard of ingested data
   - Automation of Ingestion pipeline
   - Monitor Resources (Compute, Storage, Bandwith, Time)

 #### Data Science / ML:

   - Auto-Config: frequency of ingestion, extraction parameters
   - Extract columns (datetime, indexes)
   - Detect outliers in quality of ingested data
   - Detect duplicated / derivative columns

 #### Watch out for:
   - Poor Monitoring
   - Data Loss/Overwrites
   - Misconfigurations
   - Poor ACL


 ### ETL Framework

 #### Sources

  - Change Logs
  - Data Tables
  - Data Objects

 #### Target

  - Stars (Facts and Dimension Tables)
  - Facts Tables (De-normalized)
  - Cubes (Aggregated Facts)

 #### Principles and Solutions

  - Reduce heavy joins
  - Reproducable reporting
  - Data Historical validation
  - Fast dicing/slicing of data
  - Streaming Analytics
  - Curated Glossary/Data Dictionary
  - Curated Data Access
  - Curated Data secutity/privacy
  - Rendering of Reports
  - Solving the Ad-Hoc Reports

 #### Data Science / ML:

  - Attention filtering reports
  - Smart Joins tables
  - ETL pipeline tuning

 #### Monitoring and CI-CD Pipeline:
  - Dashboard of ETL Data
  - Automate Rendering
  - Automate ETL Generation
  - Monitor Resources (Compute, Storage, Bandwith, Time)

 #### Watch out for:
   - No Curated Data
   - Poor understanding
   - Data Pollution
   - Conceptual errors
   - Poor data monitoring

 ### Data Structures

 From lower to higher abstraction levels:

  - Raw sources
  - Logs
  - Stars and Snowflakes
  - Cubes
  - Longitudinal
  - Domain Collections

 =======
 ## Data Science
 Data science must be conducted with a predictable and well defined process.  
 All experiments should be conducted according to the following steps:

  1. problem statement
  2. hypotheses and assumptions
  3. expected results
  4. sketched solution
  5. validate assumptions
  6. collect results
  7. analyze results
  8. story telling
  9. lessons learned

 Main focus on data science is to understand the why's behind the numbers. So it's very important to:
  - be critical on both results and assumptions
  - no opinions but evidence based on maths, in particular statistics
