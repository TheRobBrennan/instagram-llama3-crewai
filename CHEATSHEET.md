# Welcome

If you have just cloned this repo, please be sure to follow the `Initial setup` instructions below.

## Examples

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

### Example 1 - Use a locally-hosted LLM

This example took just shy of seventeen minutes to complete on my laptop - `16:52.86 total` officially:

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

### Example 2 - Use the Groq-hosted llama3 8-billion parameter LLM

This example took just shy of four and a half minutes to complete on my laptop - `4:24.60 total` officially:

```sh
########################
## Here is the result
########################

Your post copy:
Based on the insights gathered from the competitor analysis, I have developed three options for an ad copy for Instagram that not only informs but also excites and persuades the audience:

**Option 1:**
"Take your coffee game to the next level with our Temperature Control Coffee Mug! Say goodbye to burnt or under-extracted coffee and hello to the perfect cup every time. With our advanced temperature control system, you can adjust the temperature to your liking and enjoy the ultimate coffee experience. #TemperatureControlCoffeeMug #CoffeeLover #PerfectCup"

**Option 2:**
"Are you tired of mediocre coffee? Our Temperature Control Coffee Mug is here to revolutionize your morning routine! With its advanced temperature control system and stainless steel material, you can enjoy a perfect cup of coffee every time. Plus, our smart LED display makes it easy to monitor and adjust the temperature to your liking. #TemperatureControlCoffeeMug #CoffeeRevolution #PerfectCup"

**Option 3:**
"Experience the ultimate in coffee control with our Temperature Control Coffee Mug! With its advanced technology and sleek design, this mug is perfect for coffee connoisseurs and beginners alike. From cappuccinos to lattes, our mug can handle any type of coffee drink you desire. #TemperatureControlCoffeeMug #CoffeeControl #CoffeeLover"

Each of these options highlights the unique features and benefits of the Temperature Control Coffee Mug, while also emphasizing the target audience's pain points and interests. By using a combination of hashtags and visually appealing content, we can increase the campaign's reach and engagement.
'

Your midjourney description:
After analyzing the options for ad copy, I understand that the product is a Temperature Control Coffee Mug that allows users to set their preferred drinking temperature and keep it perfect for up to 3 hours. It's ideal for busy professionals and has a sleek design with a smart LED display. 

Based on this information, I've come up with three options for photographs that capture the essence of the product without showing the actual product:

Option 1: "A busy professional's morning routine". The photograph captures a professional, dressed in a suit, walking towards the camera, holding a cup of coffee. The background is blurred, with a subtle effect of a cityscape in the distance. The lighting is soft, with a warm glow, conveying a sense of comfort and convenience. The image is in 4K, crisp, and wide, inviting the viewer to step into the scene.

Option 2: "A moment of serenity". The photograph shows a person, dressed in casual attire, sitting on a mountainside, surrounded by lush greenery. The person is sipping a cup of coffee, with a peaceful expression on their face. The lighting is soft, with a warm color tone, evoking a sense of serenity and tranquility. The image is close-up, with a shallow depth of field, focusing the viewer's attention on the person's face and the cup of coffee.

Option 3: "A futuristic morning". The photograph depicts a modern, high-tech kitchen, with a futuristic touch. The lighting is bright, with a cool tone, conveying a sense of innovation and technology. The image captures a person, dressed in a futuristic outfit, standing in front of a sleek, high-tech coffee machine, with a cup of coffee in hand. The background is blurred, with a subtle effect of a cityscape in the distance, inviting the viewer to step into the futuristic world.

These photographs aim to capture the convenience, serenity, and innovation that the Temperature Control Coffee Mug provides, without directly showcasing the product.
python main.py  7.85s user 2.65s system 3% cpu 4:24.60 total

```

### Example 3 - Use the Groq-hosted llama3 70-billion parameter LLM

This example took just shy of twelve and a half minutes to complete on my laptop - `12:18.48 total` officially:

``` sh
########################
## Here is the result
########################

Your post copy:
Here are three options for an engaging Instagram ad copy that incorporates the key pain points of busy professionals and highlights the benefits of our temperature control coffee mug:

Option 1:
"Tired of lukewarm coffee? Our temperature control mug keeps your drink at the perfect temp for up to 3 hours, so you can focus on what matters. Say goodbye to coffee frustration and hello to a more productive you!"

Option 2:
"Busy morning? We've got you covered. Our temperature control coffee mug ensures your coffee is always at the perfect temperature, so you can power through your day with confidence."

Option 3:
"Take a break from the hustle and bustle. Our temperature control coffee mug lets you enjoy your coffee at the perfect temperature, whenever and wherever you want. Relax, recharge, and take on the day!"

Each of these options aims to resonate with busy professionals by acknowledging their pain points and highlighting how our product can solve their problems. By using relatable language and emphasizing the benefits of our product, we can create a compelling message that drives conversions.
'

Your midjourney description:
After reviewing the three options, I have decided to approve Option 1 and Option 3, and request some changes to Option 2. Here are my thoughts on each option:

Option 1: I love the concept of a busy professional taking a moment to relax and enjoy their coffee. The soft and natural lighting, warm tone, and shallow depth of field all work together to convey a sense of comfort and tranquility. The focus on the person's relaxed expression is great, and the coffee cup is subtly visible in the corner of the frame. This option is approved as is.

Option 2: While I like the idea of a serene and peaceful morning scene, I think this option needs some work. I'd like to ask the Senior Photographer to revisit this concept and make some changes. Specifically, I'd like to see a more prominent display of the coffee mug, and perhaps a few more subtle hints at the busy professional's life (e.g. a laptop or notebook in the background). I'd also like to see a slightly brighter and more vibrant color palette to make the image more engaging.

Option 3: I think this close-up shot of a person's hands cradling a warm cup of coffee is great. The soft and warm lighting, shallow depth of field, and crisp focus all work together to create a sense of comfort and relaxation. The blurred-out background of a bustling city street or office environment is a nice touch, and helps to emphasize the idea that this coffee mug is a respite from the chaos of daily life. This option is approved as is.

Here are the three reviewed options:

Option 1:
A busy professional, dressed in a sleek business outfit, sitting in a modern office with a stunning city view behind them, taking a moment to relax and enjoy their coffee during a chaotic morning. The lighting is soft and natural, with a warm tone to convey a sense of comfort and tranquility. The focus is on the person's relaxed expression, with the coffee cup subtly visible in the corner of the frame. The image is shot in 4K, with a shallow depth of field to blur the background and emphasize the subject.

Option 2 (Revised):
A serene and peaceful morning scene, with a warm golden light pouring through a large window, illuminating a cozy corner of a modern home. A laptop and notebook are scattered on a nearby table, with a steaming cup of coffee sitting beside them, prominently displaying the temperature control coffee mug. The focus is on the coffee mug, with the surrounding environment blurred to create a sense of intimacy and calm. The image is shot in 4K, with a soft focus and a warm color palette to evoke feelings of relaxation and comfort.

Option 3:
A close-up shot of a person's hands, cradling a warm cup of coffee, with a blurred-out background of a bustling city street or office environment. The lighting is soft and warm, with a shallow depth of field to emphasize the texture of the hands and the cup. The focus is on the sense of comfort and relaxation that the coffee brings, with the surrounding chaos subtly hinted at in the background. The image is shot in 4K, with a crisp focus and a natural color palette to create a sense of realism and intimacy.
python main.py  6.71s user 2.47s system 1% cpu 12:18.48 total
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
