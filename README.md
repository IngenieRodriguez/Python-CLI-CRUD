# Python-CLI-CRUD

This is a command-line interface (CLI) application written in Python that performs CRUD (Create, Read, Update, Delete) operations using a JSON file as a simple database.

## Requirements
- Python 3.x
- [Click](https://click.palletsprojects.com/) library: a Python package for creating CLI applications.
- Custom `json_maneger` module for handling JSON read/write operations.

### Setup

1. **Install Click** by running:
   ```bash
   pip install click
   ```

2. **Ensure `json_maneger.py` is available** in the same directory, with the necessary functions to read and write to a JSON file:
   - `read_json()` - Reads and returns data from the JSON file.
   - `write_json(data)` - Writes the provided data to the JSON file.

3. **Run the application** by navigating to the project directory and typing:
   ```bash
   python cli.py [command] [options]
   ```

### Available Commands

#### 1. Create a New User

Add a new user to the JSON database with `name` and `lastname` fields.

```bash
python cli.py new --name <name> --lastname <lastname>
```

**Example:**
```bash
python cli.py new --name John --lastname Doe
```

#### 2. List All Users

Retrieve and display all users stored in the JSON database.

```bash
python cli.py users
```

#### 3. Get a Specific User

Retrieve and display the user with a specific `id`.

```bash
python cli.py user <id>
```

**Example:**
```bash
python cli.py user 1
```

#### 4. Update a User

Update the `name` and/or `lastname` of a user with a specified `id`.

```bash
python cli.py update <id> [--name <name>] [--lastname <lastname>]
```

**Example:**
```bash
python cli.py update 1 --name Jane --lastname Smith
```

#### 5. Delete a User

Delete a user with a specific `id` from the JSON database.

```bash
python cli.py delete <id>
```

**Example:**
```bash
python cli.py delete 1
```

---

This CLI tool allows for quick and straightforward CRUD operations on a simple JSON file for easy data management. Adjust the filename and ensure dependencies are correctly installed to get started.
