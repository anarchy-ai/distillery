![Anarchy Logo](https://github.com/anarchy-ai/distillery/raw/main/anarchy_logo.svg) 

<p align="center">
  <a href="https://anarchy.ai/" target="_blank"><img src="https://img.shields.io/badge/View%20Documentation-Docs-yellow"></a>
  <a href="https://discord.gg/YmNvCAk6W6" target="_blank"><img src="https://img.shields.io/badge/Join%20our%20community-Discord-blue"></a>
  <a href="https://github.com/anarchy-ai/distillery">
      <img src="https://img.shields.io/github/stars/anarchy-ai/distillery" />
  </a>
</p>
<h1 align='center'> 🥃 Anarchy's Distillery 🥃 </h1>
<p align='center'><em>Shrink your models</em></p>

This is [Anarchy's](https://anarchy.ai) effort to help wean you off of closed-source models.

# Table of Contents

* [Table of Contents](#table)
* [About](#-what-is-the-distillery-)
* [Quick Start and Installation](#-quickstart-)
   * [Requirements](#-requirements)
   * [Installation](#-installation)
   * [Usage](#-usage)
* [Contributing](#-contributing-)

## 💁 What is the Distillery? 💁

If your doing one thing lots of times, why use a giant expensive and slow general purpose model when a fine-tuned small model could suffice?
Where do you get the training data? 
Why not from running a big model on user data?  
What if you don't have enough user data? 
Synthesize some with the big model.

Distillery does this.  Replace `openai.complete` or whatever with `distillery.complete` and it will 
help you automatically switch over to a custom fine-tuned model.

## 🚀 Quickstart 🚀

### 🥹 Requirements

#### Installation Requirements

Python >=3.10 Supported. Older versions of Python are on a best-effort basis. 

Use ```bash > python3 --version ``` to check what version you are on. 

To upgrade your python, either create a new python env using ```bash > conda create -n myenv python=3.10 ``` or go to https://www.python.org/downloads/ to download the latest version.

### 👨‍💻 Installation

The quickest way to get started is to run `pip install llm-vm` in your Python environment. 

Alternatively you could do this:

```bash
> git clone https://github.com/anarchy-ai/distillery.git
> cd distillery
> python -m venv <name>
> source <name>/bin/activate
> python -m pip install -e ."[dev]"
```


### ✅ Usage

```python
# import our client
from distillery.client import Client

# Select which LLM you want to use, here we have OpenAI 
client = Client(big_model = 'chat_gpt')

# Put in your prompt and go!
response = client.complete(system_prompt = '', prompt = 'What is Anarchy?', openai_key = 'ENTER_YOUR_API_KEY')
print(response)
# Anarchy is a political ideology that advocates for the absence of government...
```


## 🩷 Contributing 🩷

We welcome contributors!  To get started is to join our active [discord community](https://discord.anarchy.ai).  Otherwise here are some ways to contribute and get paid:

### Jobs

- We're always looking for serious hackers.  Prove that you can build and creatively solve hard problems and reach out! 
- The easiest way to secure a job/internship with us is to submit pull requests that address or resolve open issues.
- Then, you can apply directly here https://forms.gle/bUWDKW3cwZ8n6qsU8

### Bounty

We offer bounties for closing specific tickets! Look at the ticket labels to see how much the bounty is.  To get started, [join the discord and read the guide](https://discord.com/channels/1075227138766147656/1147542772824408074)

## 🙏 Acknowledgements 🙏

- **Matthew Mirman** - CEO
  - GitHub: [@mmirman](https://github.com/mmirman)
  - LinkedIn: [@matthewmirman](https://www.linkedin.com/in/matthewmirman/)
  - Twitter: [@mmirman](https://twitter.com/mmirman)
  - Website: [mirman.com](https://www.mirman.com)

- **Victor Odede** - Undoomer
  - GitHub: [@VictorOdede](https://github.com/VictorOdede)
  - LinkedIn: [@victor-odede](https://www.linkedin.com/in/victor-odede-aaa907114/)

- **Abhigya Sodani** - Research Intern
  - GitHub: [@abhigya-sodani](https://github.com/abhigya-sodani)
  - LinkedIn: [@abhigya-sodani](https://www.linkedin.com/in/abhigya-sodani-405918160/)
    
## License

[MIT License](LICENSE)