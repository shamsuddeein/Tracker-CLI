# Task Tracker CLI

A simple command line task manager that stores data in a `tasks.json` file in the current directory.

## Features

- Add, update, and delete tasks
- Mark tasks as `in-progress` or `done`
- List all tasks
- List tasks filtered by status: `todo`, `in-progress`, `done`
- Automatic JSON file creation if it does not exist
- Graceful error handling for invalid commands and IDs

## Requirements

- Python 3.10+ (uses only Python standard library)

## Usage

Make the script executable:

```bash
chmod +x task-cli
```

Run commands with:

```bash
./task-cli <command> [arguments]
```

Commands:

```bash
# Add a task
./task-cli add "Buy groceries"

# Update a task
./task-cli update 1 "Buy groceries and cook dinner"

# Delete a task
./task-cli delete 1

# Mark status
./task-cli mark-in-progress 1
./task-cli mark-done 1

# List tasks
./task-cli list
./task-cli list done
./task-cli list todo
./task-cli list in-progress
```

## Task Schema

Each task is stored with these properties:

- `id`: unique integer identifier
- `description`: short text description
- `status`: one of `todo`, `in-progress`, `done`
- `createdAt`: ISO 8601 timestamp
- `updatedAt`: ISO 8601 timestamp

## Data Storage

- Tasks are persisted in `tasks.json` in the directory where you run the command.
- If `tasks.json` does not exist, it is created automatically on the first write operation.
# Tracker-CLI
