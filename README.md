# API-parameters
Assignment

1) messages – What is the conversation?
What it does: Sends the conversation as a list of messages.
Structure: Each message has:
role: Who’s talking ("system", "user", "assistant").
content: What they say.
Example:

json
Copy code
"messages": [
  {"role": "system", "content": "You are a kind assistant."},
  {"role": "user", "content": "What’s 2 + 2?"}
]
Here:

The system sets the behavior: “You are a kind assistant.”
The user asks: “What’s 2 + 2?”
The assistant will reply with something like: “It’s 4.”


2) model – Which brain are we using?
What it does: Specifies the AI model you want to use.
Example:
json
Copy code
"model": "gpt-4"
This tells the API to use GPT-4, which is smarter and more capable than earlier versions like GPT-3.5.


3) max_tokens – How long should the reply be?
What it does: Sets a limit on the length of the AI’s response.
Example:
json
Copy code
"max_tokens": 50
If the AI starts explaining, it’ll stop after 50 tokens (a token is roughly a word).

4) stream – Get the reply little by little.
What it does: If true, the API sends chunks of the reply as it generates.
Example:
json
Copy code
"stream": true
Useful if you’re showing the response live, like in a chat app.

5) temperature – How creative should the AI be?
What it does: Controls randomness in responses.
Low values (e.g., 0.2): More focused and predictable.
High values (e.g., 1.0): More creative and diverse.
Example:

json
Copy code
"temperature": 0.5
If you ask:
User: “Write a poem about cats.”

Low temperature (0.2): Short, to-the-point poem.
High temperature (1.0): Quirky and playful poem with unexpected ideas.

6) top_p – How safe or bold should the AI be?
What it does: Another way to control creativity.
Low top_p (e.g., 0.1): Focuses on the most likely words.
High top_p (e.g., 1.0): Considers more creative possibilities.
Example:

json
Copy code
"top_p": 0.9
