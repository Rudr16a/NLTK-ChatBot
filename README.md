# NLTK-ChatBot
# NLTK Chat Bot

Welcome to the NLTK Chat Bot project! This project demonstrates how to build a simple chatbot using the Natural Language Toolkit (NLTK) in Python. The chatbot can engage in basic conversations and provide responses based on predefined patterns and rules.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Chatbots are widely used for customer service, information retrieval, and entertainment. This project showcases a basic implementation of a chatbot using the NLTK library in Python. The bot uses pattern matching to identify user intents and respond appropriately.

## Features

- **Pattern Matching**: Responds to user input based on predefined patterns and responses.
- **NLTK Integration**: Utilizes NLTK for natural language processing tasks.
- **Customizable**: Easily extendable with new patterns and responses.

## Installation

### Prerequisites

- Python 3.x
- NLTK library

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/nltk-chat-bot.git
   cd nltk-chat-bot
   ```

2. Create and activate a virtual environment (optional but recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. Install required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Download NLTK data (if not already installed):

   ```python
   import nltk
   nltk.download('punkt')
   ```

## Usage

1. **Run the Chatbot**:

   Open the `chatbot.py` file and run it to start the chatbot.

   ```bash
   python chatbot.py
   ```

2. **Interact with the Chatbot**:

   Type your messages in the console, and the chatbot will respond based on the predefined patterns.

## Customization

You can customize the chatbot by modifying the patterns and responses in the `chatbot.py` file. Here's an example of how to add new patterns and responses:

```python
from nltk.chat.util import Chat, reflections

pairs = [
    [
        r"my name is (.*)",
        ["Hello %1, How are you today?",]
    ],
    [
        r"hi|hey|hello",
        ["Hello", "Hey there",]
    ],
    [
        r"what is your name?",
        ["I am a chatbot created using NLTK",]
    ],
    [
        r"how are you?",
        ["I'm doing good, how about you?",]
    ],
    [
        r"sorry (.*)",
        ["It's okay", "No problem",]
    ],
    [
        r"I am (.*) (good|well|okay|ok)",
        ["Nice to hear that", "Alright, great!",]
    ],
    [
        r"(.*) (location|city) ?",
        ["I'm a bot, I exist in the digital world",]
    ],
    [
        r"quit",
        ["Bye! Take care.",]
    ],
]

chat = Chat(pairs, reflections)
chat.converse()
```

You can add more patterns and responses to make the chatbot more interactive and engaging.

## Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug fixes, please create a pull request or open an issue.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Feel free to customize this README file according to your specific project requirements and structure.
