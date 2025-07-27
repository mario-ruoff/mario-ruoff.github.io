---
collection: portfolio
title: "Telegram Message Filter"
excerpt: "A Python Flask web app to filter fetched telegram messages"
stack:
    - Python
    - Flask
    - Google Cloud
header:
    teaser: telegram-icon.png
---

## Description
This project is a Python Flask web application designed to fetch and filter messages from Telegram channels or groups, providing a streamlined way to manage and analyze message data.

## Web App
[Telegram Message Reader](https://telegram-reader.mario-ruoff.com){: .btn .btn--info .btn--large}

## Repository
[mario-ruoff/telegram-message-reader](https://github.com/mario-ruoff/telegram-message-reader){: .btn .btn--inverse}

## Task
- Find all messages in selected channels
- Filter messages with keywords list
- Analyse filter effectiveness
- Mark self-posted messages and forwarded messages

## Installation
1. Create a conda environment: `conda env create -f environment.yml`
2. Create a .env file with the following credentials:<br>
`API_ID=<your_api_id>`<br>
`API_HASH=<your_api_hash>`

## Usage
- auth_test.py: Authentication test with Telegram API
- message_reader.py: Extract messages from Telegram API into CSV file
- message_filter.py: Filter messages from keywords.txt file
