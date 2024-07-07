# Welcome

If you have just cloned this repo, please be sure to follow the `Initial setup` instructions below.

## Example 1 - Use a locally-hosted LLM

If you have this project correctly configured - and `ollama` serving the custom model we specified in the `Modelfile` - you can run this project with the following commands:

```sh
# Activate our virtual environment with the installed dependencies
% poetry shell

# Run our crew(s)
% time python main.py

```

After making sure that the proper local model was configured - and that `max_rpm` was not restricting rate limiting - here is the final result including how long the first run took on my machine:

- 2021 14" MacBook Pro
  - Apple M1 Max
  - 64 GB memory
  - 2 TB SSD
  - macOS Sonoma `14.5`
    - Node.js `v20.11.1`
    - npm `10.8.1`
    - Python `3.11.1`

```sh
########################
## Here is the result
########################

Your post copy:
**
Here are my three options for an engaging Instagram post copy:

Option 1:
"Ready to take your coffee game to the next level? Introducing our Ember Temperature Control Mug! Say goodbye to lukewarm coffee and hello to a perfect cup every time #temperaturecontrolmug #coffeeaddict"

Option 2:
"Durable, spill-proof, and perfect for daily use - that's what sets our Tempē Coffee Mug apart from the rest! Are you tired of dealing with messy coffee cups? Let us help you level up your morning routine with our Tempē Mug! #durablemug #coffeesolver"

Option 3:
"Get ready to zing up your morning! Our versatile Zing Anything Mug is designed for hot and cold beverages, making it the perfect companion for any coffee lover. Plus, its unique design will keep your drinks at the ideal temperature all day long! #zingeverything #coffeeonthe go"

These options highlight the unique features of each mug and appeal to coffee enthusiasts, encouraging engagement and potential purchases on Instagram.
'

Your midjourney description:
Based on our conversation, here are three reviewed options of photographs that align with the product's goals:

**Option 1:** "Hands-free Moment"
Description: Capture a high-tech airplain in a beautiful blue sky during a breathtaking sunset. The airplan should be in a beautiful and sleek design, with a smart LED display highlighting the temperature control feature.
In this scenario, we'll create a stunning visual that showcases the convenience of using a temperature control coffee mug while doing multiple tasks at once.

**Option 2:** "The Daily Grind"
Description: Depict an individual enjoying their morning routine with a warm, perfectly-tempered beverage from our temperature control coffee mug. The photo should be in 4K resolution, with a soft and natural lighting.
In this scene, we'll capture the moment where someone is sipping from our product while feeling refreshed and ready for the day ahead.

**Option 3:** "Caffeine-Fueled Productivity"
Description: Show an individual in their workspace, intensely focused on their laptop or papers as steam rises from a cup of perfectly-tempered beverage. This photo should be crisp and sharp, with a sense of energy and productivity.
In this scenario, we'll create a vivid visual that highlights how our temperature control coffee mug can fuel your day, allowing you to stay focused and energized.

I hope these options meet the customer's expectations!
python main.py  9.08s user 2.48s system 1% cpu 16:52.86 total

```

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

### Activate our virtual environment with the installed dependencies

```sh
% poetry shell
Spawning shell within /Users/rob/Library/Caches/pypoetry/virtualenvs/marketing-crew-LQXOd6n7-py3.11
rob@prism instagram-llama3-crewai % emulate bash -c '. /Users/rob/Library/Caches/pypoetry/virtualenvs/marketing-crew-LQXOd6n7-py3.11/bin/activate'
(marketing-crew-py3.11) rob@prism instagram-llama3-crewai % 

```

TIP: Copy and paste the full shell path - `/Users/rob/Library/Caches/pypoetry/virtualenvs/marketing-crew-LQXOd6n7-py3.11` in the above example - to be used as the path to your interpreter in VS Code.
