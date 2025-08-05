---
layout: project
title: "Telegram Message Filter"
date: 2025-04-18
imageurl: pexels-zaksheuskaya-709412-1561020.jpg
pagecolorhue: 200

stack:
    - Python
    - Flask
    - Google Cloud

links:
  - text: "Web App"
    icon: "globe"
    url: "https://telegram-reader.mario-ruoff.com"
  - text: "Repository"
    icon: "code"
    url: "https://github.com/mario-ruoff/telegram-message-reader"

excerpt: "A Python Flask web app to filter fetched telegram messages"
description: "This project is a Python Flask web application designed to fetch and filter messages from Telegram channels or groups, providing a streamlined way to manage and analyze message data."
---

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
