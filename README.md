# Rule-Based Tkinter Chatbot

A beginner Python desktop application that uses a Tkinter interface and hard-coded text commands to return simple responses, tell jokes, and open selected websites.

> **Status:** educational project. Despite the repository name, this application does not use machine learning, natural-language understanding, an LLM, or an external chatbot API.

## Features

- Tkinter chat window
- Greeting and small-talk responses
- Random joke selection
- Fixed website-opening commands
- Scrollable conversation display
- Fallback message for unsupported input

## Run

Python includes Tkinter in many standard desktop installations.

```bash
git clone https://github.com/PseudoOzone/AI-Chat-Bot.git
cd AI-Chat-Bot
python ChatBot.py
```

A desktop display is required.

## Example commands

```text
hello
how are you
tell me a joke
open google
open youtube
open whatsapp
goodbye
```

The current command matching is exact after converting input to lowercase. Variations outside the hard-coded phrases are not understood.

## Known limitations

- The code requests the `safari` browser explicitly, so website commands can fail on Windows or Linux.
- The weather command opens a fixed Chennai forecast rather than using the user's location or a weather API.
- The `open amazon` command currently opens Google.
- The input field is only cleared in one response path.
- The function name, local variable, and button reference all reuse the name `send`.
- `from tkinter import *` pollutes the namespace and makes dependencies less clear.
- Long single-line `elif` branches reduce readability.
- There is no intent parsing, fuzzy matching, conversation state, test suite, or packaging.

## Recommended improvements

- use `import tkinter as tk`
- open URLs with `webbrowser.open()` rather than forcing Safari
- store commands and responses in dictionaries
- clear the input after every submission
- bind the Enter key to message submission
- separate UI code from response logic
- add unit tests for command matching
- rename the project to reflect that it is rule-based

## License

Educational and portfolio use only unless a separate license file states otherwise.
