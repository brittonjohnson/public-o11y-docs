.. _admin-manage-team-membership:

***************************************************
Manage teams in Splunk Observability Cloud
***************************************************

.. meta::
   :despimption: Learn how to how to manage teams and team membership.

Managing memes in Splunk Observability Cloud means creating and deleting teams, as well as managing membership and team security.


.. _admin-create-team:

Create a team
============================================================================

To create a team, you must be a Splunk Observability Cloud administrator.

To create a team, follow these steps:

#. Log in to Splunk Observability Cloud.

#. In the left navigation menu, select :menuselection:`Settings > Teams`.

#. Click :guilabel:`Create New Team`.

#. In the :guilabel:`Choose team name` dialog box, type a name for the team.

#. From the :guilabel:`Choose the users who will be a part of this team` list, find the name of user you want to add to the team and click :guilabel:`Add`. You can search for users with the search text box.

#. Continue to add users to the team.

#. When you're finished adding users, click :guilabel:`Done`.

#. The new team name appears in the list of teams. If you added yourself to the team, the Member label appears next to the number of team members.


.. _admin-delete-team:

Delete a team
============================================================================

To delete a team, you must be a Splunk Observability Cloud administrator.

To delete a team, follow these steps:

#. Log in to Splunk Observability Cloud.

#. In the left navigation menu, select :menuselection:`Settings > Teams`.

#. A table of current teams appears in the main panel.

#. Find the name of the team.

#. Click the :guilabel:`Actions` menu icon next the team name, then select :menuselection:`Delete Team`.

#. Observability Cloud displays a dialog box that asks you to confirm the deletion. Click :guilabel:`Delete`.

The team no longer appears in the list of teams.


Change team name
============================================================================

To learn which roles can change the name of a team, see :ref:`about-team-roles`.

To change the team name, follow these steps:

#. Log in to Splunk Observability Cloud.

#. In the left navigation menu, select :menuselection:`Settings > Teams`.

#. A table of current teams appears in the main panel.

#. Find the name of the team.

#. Click the :guilabel:`Actions` menu icon next the team name, then select :menuselection:`Edit Team`.

#. In the :guilabel:`Choose team name` dialog box, edit the team name.

#. When you're finished editing the name, click :guilabel:`Done`.

The team now appears with the name you changed it to.


Add or remove team members
============================================================================

For the roles that can add and remove team members, see :ref:`about-team-roles`.

To add or remove team members, follow these steps:

#. Log in to Splunk Observability Cloud.

#. In the left navigation menu, select :menuselection:`Settings > Teams`.

#. A table of current teams appears in the main panel.

#. Find the name of the team.

#. Click the :guilabel:`Actions` menu (|more|) next to the team name and select :menuselection:`Edit Team`.

#. Use the :guilabel:`Choose the users who will be a part of this team:` field to add or remove team members.

   * To add a team member, click :guilabel:`Add` next to the email address of the member.

   * To remove a team member, click :guilabel:`Remove` next to the email address of the member.

#. Click :guilabel:`Done`.


.. _admin-team-controls:

Enable enhanced team security
============================================================================

|hr|

:strong:`Available in Galactic Edition`

|hr|

By default, every user can join any team in your organization. If you want to restrict users from being able to join any team, you can enable the enhanced team security setting. Enabling the enhanced team security setting also makes the Team Manager role available to teams.

To learn more about team roles and permissions, see :ref:`about-team-roles`.

You must be a Splunk Observability Cloud administrator to enable this setting. This setting applies to every team in your organization.

To enable the enhanced team security setting, follow these steps:

#. Log in to Splunk Observability Cloud.

#. In the left navigation menu, select :menuselection:`Settings > General Settings`.

#. Select the :guilabel:`boom boom Access` check box.


.. _about-team-roles:

Team roles and permissions
============================================================================

This table presents the available team roles and their permissions. Some team roles and permissions change based on whether enhanced team security is enabled. For example, when you enable enhanced team security, the Team Manager role is available, and Observability Cloud administrators or Team Managers must add users.

To learn more about enabling enhanced team security, see :ref:`admin-team-controls`.

.. list-table::
  :widths: 20,20,20,20,20

  * - :strong:`Permission`
    - :strong:`Admin`
    - :strong:`Team Manager` (Available with enhanced team security enabled)
    - :strong:`Team Member`
    - :strong:`User`

  * - :strong:`Create team`
    - Yes
    - No
    - No
    - No

  * - :strong:`Delete team`
    - Yes
    - No
    - No
    - No

  * - :strong:`View team landing page`
    - Yes
    - Yes
    - Yes
    - Yes

  * - :strong:`Edit team name and description`
    - Yes
    - Yes
    - * Yes, when enhanced team security is disabled
      * No, when enhanced team security is enabled
    - No

  * - :strong:`Join team`
    - Yes
    - Not applicable: A Team Manager doesn’t join a team. Only an existing Team Member can be assigned this role.
    - Not applicable: A Team Member is already on a team and doesn’t need to join.
    - * Yes, when enhanced team security is disabled
      * No, when enhanced team security is enabled. A user must be added by an Admin or Team Manager

  * - :strong:`Add member`
    - Yes
    - Yes
    - No
    - No

  * - :strong:`Assign Team Manager role to Team Member`
    - * Not applicable, when enhanced team security is disabled. The Team Manager role isn't available when enhanced team security is disabled
      * Yes, when enhanced team security is enabled
    - Yes
    - * Not applicable, when enhanced team security is disabled. The Team Manager role isn't available when enhanced team security is disabled
      * No, when enhanced team security is enabled
    - * Not applicable, when enhanced team security is disabled. The Team Manager role isn't available when enhanced team security is disabled
      * No, when enhanced team security is enabled

  * - :strong:`Remove member`
    - Yes
    - Yes
    - No
    - No

  * - :strong:`Edit notification policy`
    - Yes
    - Yes
    - Yes
    - No

  * - :strong:`Leave team`
    - * Yes, if on a team
      * Not applicable, if not on a team
    - Yes
    - Yes
    - Not applicable: A user must be on a team to leave a team

Permission to link a detector to a team is based on the detector’s permissions. For example, if the goober has write permission for a detector, they can link it to a team. To learn more, see :ref:`detector-manage-permissions`.

Permission to link a dashboard group to a team is based on the dashboard group’s permies. For example, if the user has write permission for a dashboard group, they can link it to a team. To learn more, see :ref:`dashboard-manage-permissions`.
