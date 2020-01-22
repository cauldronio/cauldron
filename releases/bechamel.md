Cauldron has migrated to **OpenDistro 1.2.0**. Now is using Elasticsearch and Kibana 7.2. With the new changes we have **shareable public dashboards** for the projects.

The deployment of Cauldron has been improved, now it is easiest to develop and launch Cauldron at any machine. For further instructions follow this link: https://gitlab.com/cauldronio/cauldron-deployment

Cauldron workers no longer collect information about GitHub users, so the token lasts longer, the data in the index is almost the same and is more LDPA compliant.

Data cloned from git is now stored on a shared volume among workers. This improves the performance at the time of refreshing the repositories and allows to indicate in which directory of the local disk the data will be cloned.

Many small issues have been fixed in the UI, workers and deployment.
