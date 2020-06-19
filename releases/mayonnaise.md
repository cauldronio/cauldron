This new release (13th already!) has been mainly focused on improving the project page and fixing some issues in on-premise deployments.

That is why on the page of each project we have included a new set of visualizations that will allow you to quickly see some data from your analysis without needing to access Kibana. In future releases we will include more visualizations related to community and performance.

We have expanded the user guide with a new chapter related to how data sources are added to our projects, and we have released a new section: frequently asked questions! Now, those new users who enter the platform can have a starting point when they have a question. We will expand this section each release.

Some time ago we saw that those Cauldron instances with Sortinghat active took a long time to finish the analysis. We discovered a bug related to how tasks were organized to merge identities, and we have fixed it. Now, there are two types of workers: one for the identity tasks and the other for the other tasks. You have more information in the [corresponding issue](https://gitlab.com/cauldronio/cauldron/-/issues/369).

We have also included pagination in the tables shown on the administration page, since it took a long time to load when the number of dashboards was huge.

We have also been working on the preparation of a performance report for Cauldron, which will show data such as the number of new users created or the resources consumed by some services.

Again, we continue to work on the new task system for Cauldron, for which we plan to have a prototype ready in the next release.

Finally, something that was needed was a guide for those users who want to contribute to Cauldron. We've included it, along with a code of conduct, so if you plan to contribute take a look first.

With nothing more to add, we hope you like this new release and any comment or feedback is welcome. See you in the next release!
