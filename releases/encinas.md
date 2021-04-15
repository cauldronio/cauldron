A new release of Cauldron has arrived, Encinas! It comes with some backup improvements and a notifications system.

Until now, Cauldron only allowed us to generate backups locally, and if we later wanted to take those backups to another machine we had to do it manually. Now, Cauldron has incorporated new alternatives, so that you can store your backups in an S3-compatible system. Also, it will remove automatically the older backups (> 7 days), so you don't have to mess around with storage limitations. For now, we have only tested using Spaces from DigitalOcean, and we cannot guarantee that they will work with other S3 systems.

Finally, for those users who request endless analysis we have created an option in Cauldron to notify you when the analysis have finished. When a report is ready, we will create a tweet in Twitter through CauldronBot (@CauldronBot) mentioning you and including a link to the report. Of course, to be able to use this feature, you will have to log in with Twitter during the creation of a report.

Stay tuned, and come back for the next release!

[Cauldron.io](https://cauldron.io/) Team
