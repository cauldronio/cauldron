The new Cauldron release, Iceberg, comes with new UI features and new analysis to play with in Kibana. 

Regarding the web interface, the biggest change is the project page. It has been updated with a new design that provides a better understanding on what the user should focus on. The table with all the repositories is hidden by default, and the status of the analysis and the Kibana interaction buttons have become more relevant.

We believe that one of the most important features of Cauldron is to analyze repositories. We've made some improvements to the worker's configuration and included new analysis that users were missing: 
- Github comments: activity of pull requests and issues.
- Github repository: information related with repositories like stars and followers. 
- Gitlab merge requests
- Disable git areas of code: this study related with git takes a lot to be executed. We have temporarily disabled it, maybe we will include it in the future.

We think privacy matters, that's why we are trying to migrate from Google Analytics to Matomo. We have deployed it in our servers and, depending on the results, we will make some adjustments.

We have also made many small changes to the User Interface:
 - Better share options
 - Improve projects cards
 - Update My Workspace entry page
 - Improve the documentation about the available indices
 - Fix typos
 - And much more!
 
Finally we keep improving our infrastructure. We are now working on a new cloud deployment with many machines. Our current status is the ability to deploy in Digital Ocean with Cauldron on one machine and Elasticsearch on another.

We hope you find all these new features interesting and do not hesitate to send us as much feedback as you can. See you soon with more and better features in the next release, Jelly.
