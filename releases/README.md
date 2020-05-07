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
