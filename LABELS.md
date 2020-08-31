# GitLab Labels

At Cauldron we use GitLab [labels](https://gitlab.com/cauldronio/cauldron/-/labels) to categorize and organize issues based on their nature, deadline or status, among other things.

## Planning

These labels are used for the roadmap, or to check what's the status of a tasks in a given sprint. They allow us to group tasks in meaningful columns.

From the sprint view, we have these labels:
* **Epic**: for tasks to be resolved during a sprint time. In rare occasions `epics` could last more than one sprint depending on their complexity and potential blockers. Each `epic` must be associated to a milestone.
* **Doing**: for tasks currently being resolved.
* **Blocked**: for tasks waiting for others to be resolved to resolve it.
* **Review**: for tasks resolved but waiting for someone to review the solution implemented.

From the roadmap view, we have these labels:
* **Near Term**: for features to be solved during next 3 months.
* **Mid Term**: for features to be solved in 3 to 6 months.
* **Long Term**: for features to be solved later than 6 months.

## Issue type

Each GitLab issue is tagged depending on its own characteristics. The labels used for this purpose are:
* **bug**: for glitches found in the platform.
* **feature**: for platform's features we plan to develop or requested by the users.
* **docs**: for documentation related with Cauldron in general.

## Working area or topics

These labels are used depending on the area or areas of Cauldron the task is related to. The labels used are the following:
* **Topic Infra**: for issues or tasks related to platform infrastructure like cloud environments, source code management system, issue tracker, community forum, etc.
* **Topic Backend**: for issues or tasks related to Cauldron's backend. Additionally to it, we have, to be more specific if needed:
  * **Topic Grimoirelab**: for issues or tasks related to grimoirelab that might have a link to an issue in GrimoireLab's issue tracker system.
  * **Topic Scheduler**: for issues or tasks related to Cauldron's tasks scheduler.
  * **Topic OpenDistro**: for issues or tasks related to OpenDistro for Elasticsearch
* **Topic UI**: for issues or tasks related to Cauldron's user interface. Additionally to it, we have:
  * **Topic Visualizations**: for issues or tasks related to data and metrics visualizations.
  * **Topic Kibana**: for issues or tasks related to Kibana from OpenDistro for Elasticsearch.
* **Topic Community**: for issues or tasks related to Cauldron's community (like blog posts).
* **Topic Feedback**: for issues opened by external contributors to Cauldron Team.
* **Topic Management**: for issues related to project management (like for example the discussion about which labels to use).
