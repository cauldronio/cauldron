## Orange
- Fix bug related with time axis in Bokeh charts. (https://gitlab.com/cauldronio/cauldron/-/issues/389)
- Modify some Bokeh charts that differed from Kibana ones. (https://gitlab.com/cauldronio/cauldron/-/issues/390)
- New feature: forked repositories can now be analyzed. (https://gitlab.com/cauldronio/cauldron/-/issues/392)
- Upgrade to Open Distro 1.8 and some other Python components. (https://gitlab.com/cauldronio/cauldron/-/issues/397)
- Fix bug related with scripted fields in Kibana. (https://gitlab.com/cauldronio/cauldron/-/issues/399)
- Include Bokeh time filter in the URL. (https://gitlab.com/cauldronio/cauldron/-/issues/378)
- WIP. Create visualizations and metrics related with Community of a project. (https://gitlab.com/cauldronio/cauldron/-/issues/368)
- WIP. Continue with the new system for task management. (https://gitlab.com/cauldronio/cauldron/-/issues/95)


## Nut
- New chapter for the user guide: [How to manage several projects or analysis in Cauldron](https://community.cauldron.io/t/how-to-manage-several-projects-or-analysis-in-cauldron/67)
- Improve Cauldron development processes description. (https://gitlab.com/cauldronio/cauldron/-/issues/386)
- Create a complete report with the metrics related with the evolution of Cauldron. (https://gitlab.com/cauldronio/cauldron/-/issues/384)
- My projects page is now updated automatically with the progress of the analysis. (https://gitlab.com/cauldronio/cauldron/-/issues/196)
- When you delete a project you will stay in the same page. (https://gitlab.com/cauldronio/cauldron/-/issues/320)
- Matomo installation is now optional in custom deployments. (https://gitlab.com/cauldronio/cauldron/-/issues/332)
- WIP. Create visualizations and metrics related with Community of a project. (https://gitlab.com/cauldronio/cauldron/-/issues/368)
- WIP. Continue with the new system for task management. (https://gitlab.com/cauldronio/cauldron/-/issues/95)


## Mayonnaise
- New chapter for the user guide: [Adding some data sources to my Cauldron project](https://community.cauldron.io/t/adding-some-data-sources-to-my-cauldron-project/62)
- New section in Cauldron Community: [FAQ](https://community.cauldron.io/t/frequently-asked-questions/63)
- Include new set of visualization in the project page (https://gitlab.com/cauldronio/cauldron/-/issues/368)
- Included Contributing documentation (https://gitlab.com/cauldronio/cauldron/-/issues/316)
- Include pagination in the admin page (https://gitlab.com/cauldronio/cauldron/-/issues/372)
- First approach to a Performance Report about Cauldron (https://gitlab.com/cauldronio/cauldron/-/issues/370)
- Modify workers to run Sortinghat once a day (when it is enabled) (https://gitlab.com/cauldronio/cauldron/-/issues/369)
- Fix UI bugs (https://gitlab.com/cauldronio/cauldron/-/issues/374)


## Lemon
- New chapter for the user guide: [Using Kibana in Cauldron](https://community.cauldron.io/t/using-kibana-in-cauldron/60)
- Store metrics related with the state of Elasticsearch and make them accessible for admin users. https://gitlab.com/cauldronio/cauldron/-/issues/67
- Create new visualizations in my project page using Bokeh. https://gitlab.com/cauldronio/cauldron/-/issues/361
- Include a date range picker for the visualizations. https://gitlab.com/cauldronio/cauldron/-/issues/361
- Simplify the way to add repositories into the project page. https://gitlab.com/cauldronio/cauldron/-/issues/353
- Study why the analysis of repositories is slow when Sortinghat is active. https://gitlab.com/cauldronio/cauldron/-/issues/351
- Preliminary analysis about the performance of each Cauldron page. https://gitlab.com/cauldronio/cauldron/-/issues/273
- Include a search box in the projects page. https://gitlab.com/cauldronio/cauldron/-/issues/355
- Continue with the new system for task management. https://gitlab.com/cauldronio/cauldron/-/issues/95
- Update design of public dashboard. https://gitlab.com/cauldronio/cauldron/-/issues/313
- Fix UI bugs. https://gitlab.com/cauldronio/cauldron/-/issues/352


## Ketchup
- New chapter for the user guide: [My analysis has finished! What's next?](https://community.cauldron.io/t/my-analysis-has-finished-whats-next/58)
- Show metrics and [Bokeh charts](https://github.com/bokeh/bokeh) of a project without accessing Kibana. https://gitlab.com/cauldronio/cauldron/-/issues/342
- Automatically refresh the repositories status table every 5 seconds. https://gitlab.com/cauldronio/cauldron/-/issues/278
- Repository table filter enhancements. Include multi-filters for type of data source and status, and a search box to filter by name. https://gitlab.com/cauldronio/cauldron/-/issues/284
- My projects page is now the default home page when the user is authenticated. https://gitlab.com/cauldronio/cauldron/-/issues/294
- Update the public dashboard with new visualizations related with GitLab and Meetup. https://gitlab.com/cauldronio/cauldron/-/issues/313
- Take advantage of sb-admin-2 for CSS. https://gitlab.com/cauldronio/cauldron/-/issues/334
- Update CSS to the latest version and improve mobile support. https://gitlab.com/cauldronio/cauldron-web/-/merge_requests/121
- Import new index patterns into existing Kibana workspaces. [More info](https://gitlab.com/cauldronio/cauldron/-/blob/master/guides/indices_information.md)
- Store metrics related with Cauldron in ElasticSearch (daily users, daily completed tasks, etc.). https://gitlab.com/cauldronio/cauldron/-/issues/346
- Create a Matomo link for admin users. https://gitlab.com/cauldronio/cauldron/-/issues/350
- Continue with the new system for task management. https://gitlab.com/cauldronio/cauldron/-/issues/95
- Fix "popular projects" links. https://gitlab.com/cauldronio/cauldron/-/issues/348


## Jelly
- New metrics, daily and monthly
- Possibility of deploying Cauldron on 3 hosts
- Syslog logs are now also saved in Elasticsearch
- New Ansible playbook to provision remote hosts
- Terraform templates have been modified
- `git-demography` study has been disabled
- New aliases for Elasticsearch indices
- Upgrade to Open Distro 1.6
- First user guide released
- Fix minor bugs


## Iceberg
- Redesign project page with a more intuitive header
- We can deploy in 2 machines in Digital Ocean
- New analysis included in Cauldron like gitlab merges, github comments and github repo
- Matomo + syslog is ready to be used in production
- Redesign of projects cards to include more detailed information
- Improved the way to share dashboards
- Create documentation about indices
- Updated visualizations for Kibana
- Many bugs fixed related with the UI


## Honey
 - Anonymous data in enriched and raw indices
 - Creation of My workspace
 - Terraform templates to deploy on DigitalOcean
 - Usage of Syslog for log collection
 - Minor fixes


## Ginger
 - Option to remove Sortinghat from Grimoirelab
 - New status page for Cauldron
 - Social share buttons on project overview
 - Repository table improvements
 - **(WIP)** New Task Management system
 - **(WIP)** Cloud migration
 - **(WIP)** Substitution of Google Analytics by Matomo
 - Fix some bugs


## Foie
- Data from GitHub now is enriched correctly
- User and password is not needed for Hatstall
- Pagination for the project page
- Pagination for the projects page
- Create and test snapshots
- Remove Archimedes and use a simpler way to import visualizations
- Migrate to Opendistro 1.4.0
- Migrate to Django 3.0
- Update the token request message
- Set admin users from the inventory variables
- Minor fixes


## Emmental

- Migrate to ODFE 1.3.0
- Migrate to Django 2.2
- Allow upgrade/downgrade admin users from the admin page
- New Cauldron public dashboard
- Allow user deletion from the admin page
- Allow account deletion from the settings page
- Allow Dashboard deletion
- Enable the analysis of repositories inside Gitlab groups
- Smart Navigation Menu
- Set up a public status page
- Cauldron forum
- Minor fixes


## Dijon

- New settings page for managing the tokens and username
- New home page
- New user projects page
- Cauldron newsletter
- New panels for Kibana (will change in a near future)
- Updated the header of a project page
- Migrate from alpha.cauldron.io to cauldron.io
- Move the group from cauldron2 to cauldronio
- Fix typos


## Curry

- Include Hatstall
- Add datatables
- Select the backend to be analyzed from the "add datasource" input
- Force refresh repositories when they are added to a project
- Make Google Analytics module optional
- Include version name in the logo
- Fix log issues


## Bechamel

- Migrate to Opendistro 1.2.0
- Create public dashboards
- New deployment with ansible playbooks
- UI changes in projects list and main page
- Do not collect GitHub user info from mordred
- Modify the path where the git projects are cloned
- Fix UI issues
- Fix mordred and token issues
- Fix deployment issues
