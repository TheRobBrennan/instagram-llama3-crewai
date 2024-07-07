# Welcome

## Initial setup - macOS

### Install Poetry

You can make sure Poetry is installed by running the following:

```sh
# Install Poetry
% curl -sSL https://install.python-poetry.org | python3 -

# Verify Poetry is installed
% poetry --version
Poetry (version 1.8.3)
```

### Create our own local model for experimentation

Let's use the model definition at `./Modelfile` and create a new local model to use:

```sh
# List available models on our machine
% ollama list
NAME            ID              SIZE    MODIFIED       
llama3:8b       365c0bd3c000    4.7 GB  16 minutes ago

# Create a custom model based on our definition
% ollama create crewai-llama3-8b -f ./Modelfile

# List available models on our machine and verify our new model is created 🤓
% ollama list
NAME                    ID              SIZE    MODIFIED       
crewai-llama3-8b:latest e24ebf105f8e    4.7 GB  13 seconds ago
llama3:8b               365c0bd3c000    4.7 GB  17 minutes ago

```

### Setup our development environment

```sh
# Install dependencies from pyproject.toml
% poetry install --no-root

```
