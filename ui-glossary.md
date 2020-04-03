This is a glossary with the keywords used in the Cauldron UI:

* **Project**: the scope of the development community and processes analysis the user wants to perform. It's defined by the Project Name, the Data Sources, and their repositories. Cauldron provides one Project Name automatically, but the user shall be able to change it.
* **Data Source**: each one of the platforms Cauldron gathers information from. By now, Cauldron supports: git, Github, GitLab, and Meetup as Data Sources. Users shall be able to add multiple Data Sources to a project.
* **Repository**: each one of the unique points of information Cauldron gathers information from for each Data Source. For example, a GitLab repository URL, or a Meetup group URL.
* **Public Dashboard**: A public collection of predefined visualizations of metrics related with development community and processes for a given project.
* **My Workspace**: User's private data visualization dashboard instance to build custom visualizations and dashboards.
* **Status**: When gathering data from a repository, there are 5 potential states:
  * **Pending**: Cauldron has not started any data gathering or data processing.
  * **Running**: Cauldron is gathering and processing data from a repository.
  * **Completed**: Cauldron has finished gathering and processing all the data from a repository.
  * **Error**: Cauldron has finished and it got an error during the data gathering or processing.
  * **Unknown**: Cauldron does not have a task associated with this repository. Neither pending nor completed.
* **Refresh**: Users shall be able to refresh data from repositories.
* **Logs**: Users shall be able to review the information and records about the events during the repositories data gathering and processing.

This affects several parts of the UI (buttons, messages, etc.)
