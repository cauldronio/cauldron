We have reached the tenth release of Cauldron, Jelly, with a lot of news focused mainly on improving the infrastructure and the back-end of the platform.

We are aware of how important it is to know the state of health of your favorite projects. In the same way, it is interesting to know the health status of your instance of Cauldron, so we have included some commands that will allow you to obtain daily and monthly metrics on some interesting aspects of Cauldron, such as the number of users created or the number of tasks completed.

Once again, we are approaching a total division of Cauldron into multi-host services, allowing deployment on 3 different machines: one to host the Elasticsearch service (as in the previous release), another to host the web server service and workers, and a third for the rest of Cauldron's services.

Related to the above, provisioning resources for remote deployments is now being done with Ansible (previously it was done with Terraform).

Related to Open Distro, the logs collected by syslog are now also saved in Elasticsearch (for a possible future display in Kibana), and we have updated some aliases. By the way, we have updated the Open Distro version to version 1.6!

We had some performance issues with one of the GrimoireLab analysis introduced in the previous release, the so-called `git-demography`, so we have disabled it.

Finally, we have created the first user guide for Cauldron, in which we detail the steps to follow to create our first project in Cauldron!

We hope these updates improve your experience with Cauldron, and we'll see you soon in the next release!
