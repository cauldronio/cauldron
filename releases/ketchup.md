The new release of Cauldron, Ketchup, brings new UI features that could simplify your process of visualizing your projects.

First of all we have added a new chapter to the user guide: [My analysis has finished! What’s next?](https://community.cauldron.io/t/my-analysis-has-finished-whats-next/58). Have a look later!

The first change you will notice when you log in to Cauldron after authenticating will be that the main page will be your list of projects. With this change, we want to make sure that the way to access your projects and create new ones is easier.

On the page of a certain project we are trying new things (still in development). We have incorporated a few metrics, which will be more in future versions. It shows the status of a project without the need to access Kibana.

The table of repositories for a project (hidden by default) has new updates. It is updated every 5 seconds to avoid reloading the page, and new filters have been added that allow obtaining more detailed results.

The Kibana public dashboard has been updated to include new GitHub, GitLab and Meetup visualizations at the bottom.

The CSS of the page has been updated including `sb-admin-2`. Some elements have also been repositioned so they can be displayed better on smaller screens.

In the internal part of Cauldron we continue implementing a new worker system to improve the performance of certain tasks, and we are improving the collection of metrics to better understand the evolution of Cauldron without affecting the privacy of users.

Finally mention that we have updated the index-patterns in Kibana, [you can take a look here](https://gitlab.com/cauldronio/cauldron/-/blob/master/guides/indices_information.md#index-patterns-for-kibana). We recommend not creating new visualizations with the `deprecated` index patterns, as they may be incompatible in the future.
