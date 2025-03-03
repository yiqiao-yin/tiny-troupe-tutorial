# tiny-troupe-tutorial

🚀 **Welcome to the Tiny Troupe Tutorial!** 🚀 This guide will help you get started with the `tinytroupe` package, which allows you to create and interact with virtual personas in Python. Follow these steps to dive into a world of creative programming!

### Step 1: Clone the Repository
Start by cloning the Tiny Troupe repository from Microsoft. This contains all the code you need to get started.

```bash
git clone https://github.com/microsoft/tinytroupe
cd tinytroupe
pip install .
```

### Step 2: Set Up Your Environment
Before running the scripts, set up your environment variable for the OpenAI API key. Replace `"xxx"` with your actual API key.

```bash
export OPENAI_API_KEY="xxx"
python
```

### Step 3: Create Lisa the Data Scientist
Now, let's create Lisa, a virtual data scientist. She can perform tasks and respond to queries about her life! 🧠✨

```python
from tinytroupe.examples import create_lisa_the_data_scientist

# Instantiate a Lisa from the example builder
lisa_ds = create_lisa_the_data_scientist() 
lisa_ds.listen_and_act("Tell me about your life.")
```

### Step 4: Meet Yiqiao, the Engineer
Introduce yourself to Yiqiao, a character you can customize. Below, you'll define his attributes and professional background. Feel free to tweak the details!

```python
from tinytroupe.agent import TinyPerson

# Create your own tiny person named Yiqiao 🚀
yiqiao = TinyPerson("Yiqiao")

# Define basic attributes (make sure to keep it fun!)
yiqiao.define("age", 35)  # Yiqiao is wise beyond his years! 🦉
yiqiao.define("nationality", "Chinese")  # Proudly representing his roots 🌏
yiqiao.define("occupation", "Engineer")  # Building the future, one line of code at a time 🛠️

# Define professional history and routine
yiqiao.define("professional_history", "Yiqiao has been in the AI/ML space since 2015, leading AI-backed solutions, including Computer Vision, Natural Language Models (NLP), Large Language Models (LLMs), and Generative AI.")
```

This README aims to guide you through setting up and experimenting with the `tinytroupe` library, enhancing your Python projects with virtual personas that can act and interact based on the attributes you define. Have fun coding and experimenting! 🌟