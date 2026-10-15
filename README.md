# AI Research Agent:

A console-based research assistant built using Python and LangChain. The user types in a topic, and the agent searches Wikipedia and the web using Claude to display a structured summary with the tools it used and sources. The user also has the ability to save this output in a text file.

Created by following Tech With Tim's AI agent tutorial on YouTube.

## What it does:

- Receives a research question or topic from the terminal.
- Uses tools such as Wikipedia, DuckDuckGo search and a save-to-file tool.
- Returns a specific output structure including the topic, summary, sources and tools used.

## Setup:

- Step #1: Clone the repo and create a virtual environment:
  python3 -m venv venv
  source venv/bin/activate
- Step #2: Install dependencies: pip install -r requirements.txt
- Step #3: Copy '.env.example' to '.env' and add your own Anthropic API key.
- Step #4: Run: python main.py

## Example:

Query: What is the capital of Sweden?

'''
topic='Capital of Sweden'
summary="The capital of Sweden is Stockholm. It is also the country's most populous city."
sources=['Wikipedia: Stockholm (https://en.wikipedia.org/wiki/Stockholm)']
tools_used=['wikipedia']
'''

Note: Output can contain mistakes. Verify facts using the sources.

## Changes made from the tutorial:

- Migrated the code to current LangChain due to video using outdated version (agents moved to 'langchain_classic').
- Fixed a minor parsing bug where the model would occasionally reply with a "thinking" block to begin with instead of text, resulting in a KeyError.
- Updated the model to a current Claude model ('claude-haiku-5-5')

## Tech:

Python, LangChain, Anthropic Claude API, Pydantic.

## Credit:

Based on the AI agent tutorial by Tech With Tim.
