# OpsDesk CLI

![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![Architecture](https://img.shields.io/badge/Architecture-Layered-success)
![Storage](https://img.shields.io/badge/Storage-JSON-informational)
![Testing](https://img.shields.io/badge/Testing-pytest-success)

OpsDesk CLI is a terminal based productivity application for managing contacts and notes with persistent local storage, validation, search, tagging, and automated tests.

I worked on this as part of a team Python project. The application follows a layered structure so domain models, business logic, storage, validation, and CLI behavior remain separated and easier to test.

## What it does

### Contacts

* add, edit, search, list, and delete contacts
* store multiple phone numbers
* store optional email, address, birthday, notes, and tags
* show upcoming birthdays
* search contacts by partial match

### Notes

* add, edit, search, list, and delete notes
* attach tags
* search by one or multiple tags
* support any or all tag filtering

### Reliability and validation

* validates phone numbers and email addresses
* validates birthdays and required fields
* persists data in JSON
* handles damaged storage files with backup behavior
* provides command aliases and interactive help
* includes automated tests with pytest

## Stack

* Python 3.11+
* pytest
* JSON storage
* phonenumbers
* email-validator
* prompt-toolkit

## Architecture

The project separates responsibilities across:

* domain models
* service and business logic
* repository and storage layers
* validation
* CLI interaction
* shared utilities

That structure keeps the command layer thin and makes the core behavior easier to test independently.

## Run locally

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the project:

```bash
pip install -e .
```

Run it:

```bash
assistant-bot
```

Run the tests:

```bash
pytest
```

## Team

This project was built collaboratively by:

* Andrii Triapitsyn
* Iryna Zvirkovska
* Valeriy H
* Oksana Levchenko

## Why I keep it in my portfolio

Most of my day to day work is infrastructure focused, so I wanted one project that shows I can also structure and test an application in Python. It gives me a useful codebase for practicing packaging, validation, persistence, testing, and maintainable application structure.
