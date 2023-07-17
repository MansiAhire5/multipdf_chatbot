# Multi Document Reader and Chatbot using LangChain and OpenAI






`multi-doc-chatbot.py` Can handle interacting with multiple different documents and document types (.pdf, .dox, .txt), 
and remembers the chat history and recent conversations.
It uses embeddings and vector stores to send the relevant information to the LLM prompt. Also provides a chat interface
via the terminal using stdin and stdout. Pressing `q` helps escape the chat window.

Architecture:
![image](https://github.com/MansiAhire5/multipdf_chatbot/assets/109126368/7c8ebf7b-37a4-40f2-9519-6b5cd14a8705)

After setting up the virtual environment, and installing the required packages

```
git clone git@github.com:smaameri/multi-doc-chatbot.git
cd multi-doc-chatbot
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
```
`cp .env.example .env`

We should copy an OpenAI API key into the `.env` file, and save the file. It should send up looking something like

`OPENAI_API_KEY=sk-`


We will place any files you would like to
interact with inside the `/docs` folder. Enter `q` to exit the prompt at any time.

```python
python3 multi-doc-chatbot.py
```

To improve the chatbot, possibilities could include optimizing the prompt
templates, using different LLMs which can accept more tokens and context lengths, creating an agent to refine the results,
and whatever else you can think of 
