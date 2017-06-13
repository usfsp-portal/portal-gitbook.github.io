O
SSP History
ossp_history
This table stores a list of changes made to different parts of the portal. It includes six columns:

id: An auto-incrementing field
id_user: The ID of the user who made the change
id_action: The type of change made
id_record: The particular entry changed
value: The old, or original value
stamp: The date and time of the change
id_action
This field holds an integer value. Possible values are finite, and each represents a specific action, as defined here:

1: Update the title/label of a chat room.
2: Change the status of a chat room from one value to another.
3: Change the role of a user in a chat room.
4: Delete access to a specific chat room for a specific user.
5: Delete a user from a unit.
6: Give a unit access to a specific room.
7: Delete a unit's access from a specific room.
id_record
This field holds the ID of the record that was updated or deleted. Depending on the nature of the change, the record may come from different tables.

value
This field holds different information depending on the action performed. Please review to the notes below:

4 (Delete Chat Room Access): When users are removed from chat rooms, we capture both the room and user IDs in this field. We separate the values with a colon. For example: 
1136:12345

Here, 1136 is the room ID, and 12345 is the user ID.
