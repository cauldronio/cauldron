In this release we have been mainly focused on improving our infrastructure and fixing bugs in the data collected.

In our path to improve the data consistency and privacy laws comply, we have seen that some fields were missing in the GitHub enrichment process. In this version, we have fixed that issue and from now, all the data collected from the mentioned backend will be accurate. We will have to erase all the data to make sure it is consistent. A notice will appear on the Cauldron page in the next few days. 

We are also working on improving on-premises deployments. In this topic we have completed the integration of Cauldron and Hatstall. Both are using the same accounts and from now on it is not necessary to use of a different username and password. 

The user interface is another of our priorities. For the management of projects and repositories we have modified the pagination system we already had, that will allow us to perform simpler actions on server side and offer more features in the next version. We have disabled temporarily the search box.

As of now, Cauldron has backup copies of all the data that will help us to recover from an unwanted state and also migrate to a new cloud infrastructure to scale the system.

Cauldron is using from this version [Opendistro 1.4.0](https://github.com/opendistro-for-elasticsearch/opendistro-build/blob/master/release-notes/release-notes-odfe-1.4.0.md) and [Django 3.0](https://docs.djangoproject.com/en/3.0/releases/3.0/) 

Finally we have fixed minor bugs in the code, simplified the way to import panels to Kibana and updated some text in the UI. 