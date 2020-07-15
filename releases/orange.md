The new Cauldron release, Orange, is a small update. Some small features have been included and some known issues have been fixed.

Regarding the new features, Cauldron now allows the analysis of forked repositories so that you can know the state of their health.

Also, time filtering of Bokeh charts has been included in the URL to make possible the sharing of these charts with their corresponding time range.

Related with Bokeh charts, we have fixed some bugs:
 - The first one did not show one of the graphs well, and its corresponding version in Kibana was different (We are speaking about the hourly commit chart).
 - The second did not correctly display the selected time ranges when there was no data at the beginning or end of these ranges.

We noticed that the scripted fields in Kibana were not being exported correctly along with the index patterns, which caused failures in those imported dashboards that used them. This issue has been resolved and should no longer fail with new exported dashboards.

We continue to work on the new task management system, which we plan to have on the testing servers before the end of August.

Also, the new visualizations for Bokeh have suffered a slight delay and will be released in the next release.

Finally, we have updated the Open Distro version to 1.8, as well as various Python components that we use in Cauldron.

Despite being a small update, we hope that these fixes will enhance your experience with the platform!
