
Chat Access

chat_access

This table monitors who has access to what chat rooms and what level of access they have. It includes five columns:

id: An auto-incrementing field
id_user: The user given access
id_room: The room to which the user is given access
id_role: The level of access granted to the user
stamp: The date and time access is granted to the room
id_role
This field holds an integer value mapped to a set of privileges. Possible values are as follows:

1: Hidden Observer: You can't type, and you aren't seen
2: Observer: You can't type, but you appear in the list of attendees
3: Participant: You can type, and you appear in the list of attendees
