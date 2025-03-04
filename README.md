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

### Step 4: Create Conversation Proxy

In this step, we create multiple personas to simulate a dynamic and realistic conversation environment. We use `TinyPerson` class from the `tinytroupe` module to define these personas. Each persona has specific attributes like age, nationality, and occupation, along with a detailed professional history. This helps in crafting more nuanced and realistic interactions within the simulation.

```python
from tinytroupe.agent import TinyPerson
from tinytroupe.environment import TinyWorld
```

Let's define the first persona: `jon`. Jon is portrayed as a dedicated director of a non-profit organization focused on helping the homeless. 🏠

```python
jon = TinyPerson("Jon")

# Define basic attributes
jon.define("age", 45)  # 📝 Adjust the age to fit the scenario
jon.define("nationality", "American")
jon.define("occupation", "Director of a Non-Profit Organization for Homeless Shelters")

# Define professional history and routine
jon.define("professional_history", """
Jon has dedicated over 20 years to advocating for social causes, particularly addressing homelessness.
He currently serves as the Director of a non-profit organization focused on building and maintaining homeless shelters across the United States.
Jon actively seeks government funding and collaborates with local communities and policymakers to create sustainable solutions for those in need.
""")
```

Next, we introduce another persona: `chris`. Chris is a seasoned congressman responsible for approving funding proposals, adding a layer of governmental insight into the simulation. 🏛️

```python
chris = TinyPerson("Chris")

# Define basic attributes
chris.define("age", 50)  # 📝 Adjust the age to fit the scenario
chris.define("nationality", "American")
chris.define("occupation", "Congressman in Charge of Approving Funding Proposals")

# Define professional history and routine
chris.define("professional_history", """
Chris has served as a Congressman for over 15 years, representing a diverse constituency.
As part of his duties, he oversees the evaluation and approval of government funding proposals,
including those aimed at social initiatives like homeless shelters.
Chris has a reputation for being pragmatic and data-driven in his decision-making.
""")
```

By setting up these detailed personas, we can simulate interactions that are reflective of real-world decision-making processes in social policy and government funding. This setup allows for a rich exploration of dialogue and interaction dynamics within the simulated tiny world environment.
