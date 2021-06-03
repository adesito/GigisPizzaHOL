[![](./images/image1.png)](https://www.oracle.com/code-one/)

# Gigi's Polls - GitOps and LiquiBase HOL
This HOL is based in a Demo developed by Spain Presales Tech Team as part of an innovation initiative to approach Oracle Cloud Solutions by providing practical examples that could be “touched” and easily understood.

Demo is known as Gigi’s Pizza. This Use Case is focused in GitOps and LiquiBase. In Gigi's Pizza demo we have three microservices coded in different languages like nodejs and of course Java (Helidon framework). This three microservices are part of a delivery pizza app, one microservice controls the orders, other one controls the pizza delivery and the last one controls the accounting. 

![](./images/gigis-architect-original-2.png)

In the first demo version, we don't have any feedback from the customer that receive a pizza, so imagine that the marketing and business areas want to know that feedback to improve the pizza delivery service or to create new pizza types. To create this new feedback service we have to modify the SQL DB PDB adding new tables in the squema and several fields in the tables. To create a DB squema version we will use LiquiBase, a software that let you create squema versions. We could return to a previous version of the Data Base after a failure or bad feeback of an app version (canary deployment for example) in an easy way with LiquiBase that is included with Oracle SQLPlus software.

![](./images/gigis-architect-polls.png)

This GitOps Hands On Lab includes:

* Oracle Visual Builder Studio.
* LiquidBase included in Oracle SQLPlus software.
* Oracle Cloud Infraestructure: 
  * Compute
  * Networking
  * Resource Manager (Terraform as a service)
  * DBCS

# In this Hands on Lab

All HOL was written in English and all the screenshots are in English Language. We recomend you that select English as your default language in Oracle Cloud. Select the Earth Icon at the top right (near your profile icon) and change the language to English.

In this HOL you will create a poll app for customer feedback.

You will:

* Create a new feedback webpage with Oracle Visual Builder Studio.
* Modify the current microservices to include the new Data.
* Deploy webapp in a separate server (IaaS compute) instead of use the internal Visual Builder server to improve cost savings.
* That deploy will be use terraform and sh scripts to automate it. 
* All deployment files (terraform + sh + liquibase scripts) will be in a GIT repo (GitOps).
* Create the jobs and pipelines to deploy the app and modify the Data Base.
* Create the jobs and pipelines to delete the app and return the Data Base to initial state.

