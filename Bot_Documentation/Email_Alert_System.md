E
mail/SMS Alert System
This alert system sends automatic messages in email or SMS formats. The format used depends on an individual user's preferences.

Alert Types
The following alert types are possible:

'New Question' Alerts
Alert Fires: When a student asks a new chat question
Who Gets the Alert: Members of role group '10'
Alert ID: 1
Additional ID/Data Sent to Server: Chat Room/Question ID
'Routed to a Unit' Alerts
Alert Fires: When a router assigns a question to a one or more units
Who Gets the Alert: Users who are also members of the unit and have role IDs of '5'
Alert ID: 2
Additional ID/Data Sent to Server: Chat Room/Question ID
'Routed from a Unit' Alerts
Alert Fires: When a unit member transfers ownership of a question to a different unit
Who Gets the Alert: Users who are members of either unit ('from' or 'to') and have role IDs of '5'
Alert ID: 3
Additional ID/Data Sent to Server: Chat Room/Question ID
'Summary' Alerts
Alert Fires: At the end of each day
Who Gets the Alert: Members of role group '10'
Alert ID: 4
Additional ID/Data Sent to Server: None
Response Provided Alerts
Alert Fires: When a support staff member responds to a question
Who Gets the Alert: The user who asked the question
Alert ID: 5
Additional ID/Data Sent to Server: Chat Room/Question ID
Sample Alerts
Here's a typical alert call:

//Send a "New Question" alert for Question ID 3245...
alert_system(1, 3245);
