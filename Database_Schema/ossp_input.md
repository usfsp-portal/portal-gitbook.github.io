O
SSP Input
ossp_input
This table captures input from the "Have a question?" box. This input field appears on the homepage of the portal and via widgets. It provides information about what users are asking, what kind of responses they're getting, and what they decide to do next. It will become an important source of data that informs refinements to the bot technology and provides managers with a view of where and how students are asking their questions. It includes 8 columns:

id: An auto-incrementing field
id_user: The user ID asking the question
input: The question asked
origin: From where the question was asked
modality: How the question was asked
response: Whether the system provides an automated response
reaction: What the user does after receiving the response
stamp: The date and time the question is asked
input
This field holds the text that the user supplied, and provides data for continuously improving the automated responses for the bot.

origin
This field holds an integer the maps to a unique location. Possible values include the following:

0: Homepage of online.usfsp.edu
1: Future widget (e.g., Library homepage, Journalism site)
modality
This field holds an integer that maps to the manner in which the question was asked:

0: The question was typed
1: The question was spoken (using browser-based speech recognition)
2: Future modality
response
This field holds an integer of either 0 or 1.

0: The system was unable to provide an automated response. ("We can't seem to find the answer to that question.")
1: The system was able to provide an automated response.
2: The system asked a clarifying question to determine what the user wants to know.
reaction
This field holds an integer that maps to the action the user takes upon receiving a response:

0: No detectable action taken
1: The user starts a chat session
2: The user clicks to browse for an answer
