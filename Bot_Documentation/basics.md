B
asics
Basic Flow
Speech-to-Text (If Applicable)
Spell Check (We might cleanup typos automatically -- something like Google's "Did you mean?" feature)
Determine whether the question can be answered. This entails figuring out which Knowledge Bank should be used. If the question can't be answered, provide a relevant prompt to the user. This step involves pattern matching. We check to see whether the question contains the right mix of words and phrases, in the right order, to fit one of our predefined patterns. Many questions will require data from more than one bank.
Determine what the user is asking and reassemble the query into a function call that can run against the bank.
Gather relevant contextual data based on factors such as the current date and the user's profile.
Query the knowledge bank, retrieve the results, and format them into a human-readable format.
Display the answer to the user.
Knowledge Banks & Sample Questions
"Hour" Questions
When does the library open today?
What time does the library close tonight?
What are the library hours this semester?
What are the hours for the library?
What are the hours for Poynter Library next semester?
What's tomorrow's opening time for the library?
What's the opening time for the library tomorrow?
"Schedule" Questions
When does the fall semester start?
What's happening on campus this week?
What's the last day to register for classes?
When is commencement?
When does homecoming happen?
When is the add/drop deadline?
"Course" Questions
What's the journalism department offering in the fall?
What classes will psychology offer online next semester?
What classes in my department are still open?
Who's teaching English 101 in the fall?
What evening classes does Journalism and Media Studies offer this semester?
"Contact" Questions
What's the number for the registrar?
What's a good email address for the student success center?
How can I reach academic services?
"Catalog" Questions
How many credit hours do I need to be classified as a sophomore?
Supplemental Knowledge Banks
These banks are not queried directly, but they are necessary for the primary banks to function.

Units. A list of all departmental units across campus.
Contextual Data
Contextual data allow the system to substitute actual values for phrases like "next semester," "this semester," "today," "tomorrow," "right now" and "my department."

Contextual data take two basic forms: environment and user.

Environment Contextual Data
Current date and time
User Contextual Data
Department
Major
Classification
In/Out Of State
