## Fields exported in CSV files

Cauldron allows its users to download some of the data analyzed as a CSV file. Each data source in Cauldron has different exported fields:

## Git

- **hash**: Commit hash.
- **repo_name**: Repository name.
- **author_uuid***: Author UUID from Sortinghat.
- **author_domain**: Domain associated to the author in SortingHat profile.
- **author_date**: Author date (when the original author made the commit).
- **utc_author**: Author date (when the original author made the commit) in UTC.
- **tz**: Timezone in which the commit was made by its original author.
- **commit_date**: Date when committer made this commit.
- **utc_commit**: Commit date in UTC.
- **committer_domain**: Committer domain.
- **files**: Number of files touched by this commit.
- **lines_added**: Number of lines added by this commit.
- **lines_removed**: Number of lines removed by this commit.
- **author_name****: Author name.
- **author_org_name****: Author organization name from SortingHat profile.

## GitHub

- **repository**: Repository name.
- **id**: Issue's ID in GitHub.
- **pull_request**: True/False if the item is a pull request or not.
- **url**: Full URL of the issue.
- **created_at**: Date when an issue was opened.
- **closed_at**: Date when an issue was closed.
- **state**: State of the item (open/closed).
- **author_uuid***: Author's UUID from SortingHat profile.
- **assignee_data_uuid***: Assignee's UUID from SortingHat profile.
- **user_name****: User's name.
- **user_org****: User's organization name.
- **user_location****: User's geographical location.
- **assignee_login****: Assignee's login name from GitHub.
- **assignee_domain****: Assignee's domain name from GitHub.
- **assignee_data_org_name****: Assignee's organization name from SortingHat profile.
- **author_domain****: Author's domain name from SortingHat profile.
- **author_name****: Assignee's name from GitHub.
- **author_org_name****: Author's organization name from SortingHat profile.

## GitLab (Issues)

- **repository**: Repository name.
- **id**: Issue Id in GitLab.
- **id_in_repo**: Issue Id in the repository it belongs to.
- **state**: 'opened' or 'closed'.
- **created_at**: Date in which the Issue was created.
- **closed_at**: Date in which the Issue was closed.
- **time_to_first_attention**: Time from creation to first comment or reaction (whatever occurs first) added by an author different from the one who created this Issue.
- **author_username***: Author user name from GitLab.
- **assignee_username***: Assignee user name from GitLab.
- **milestone**: Assigned milestone.
- **author_name****: Author name.
- **author_org_name****: Author organization name.
- **assignee_name****: Assignee name.

## GitLab (Merge Requests)

- **repository**: Repository name.
- **id**: Merge Request Id in GiLab.
- **id_in_repo**: Merge Request Id in the repository it belongs to.
- **state**: 'merged', 'opened' or 'closed'.
- **created_at**: Merge Request creation date.
- **closed_at**: Date when the merge request was closed.
- **solved_at**: Date when the merge request was merged or closed.
- **time_to_first_attention**: Time from creation to first comment or reaction (whatever occurs first) added by an author different from the one who created this Merge Request.
- **author_username***: Author user name from GitLab.
- **merge_author_login***: Merge author login from GitLab.
- **milestone**: Assigned milestone.
- **author_name****: Author name from SortingHat.
- **author_org_name****: Author organization name from SortingHat.
- **merge_author_name****: Merge author name from GitLab.

## Meetup

- **id**
- **group_id**
- **type**
- **event_url**
- **like_count**
- **meetup_created**
- **meetup_duration**
- **meetup_status**
- **meetup_time**
- **meetup_updated**
- **meetup_yes_rsvp_count**
- **member_is_host**
- **num_comments**
- **num_rsvps**
- **rsvps_limit**
- **rsvps_response**
- **time_date**
- **venue_address_1**
- **venue_city**
- **venue_country**
- **venue_name**
- **group_members**
- **group_name**
- **group_topics**
- **author_id***
- **author_uuid***
- **author_user_name****
- **member_id****
- **member_name****

## StackExchange

- **origin**
- **tag**
- **type**
- **item_id**
- **creation_date**
- **author***
- **author_reputation**
- **score**
- **down_vote_count**
- **up_vote_count**
- **answer_count**
- **comment_count**
- **favorite_count**
- **question_has_accepted_answer**
- **question_tags**
- **view_count**
- **tag**
- **answer_status**
- **is_accepted**
- **question_id**
- **question_tags**

\*: Since these fields have personal information of the users, they are encrypted to comply with the GDPR. An unencrypted version of these fields can be acquired by hosting an instance of Cauldron or by purchasing a subscription at [Cauldron Cloud](https://cloud.cauldron.io/).

\**: These fields are only available in the [Cauldron Cloud](https://cloud.cauldron.io/) version.
