## Details about the virtual environment
The following are detailed instructions for deploying the virtual environment for AI Agents.

The first option is to clone this repository and follow the steps described in the README file.

These instructions are intended to show you how to test the Jupyter Notebooks individually in a virtual environment.

### What is a virtual environment?
Deploying a virtual environment is the best practice for anyone doing Python development, especially with automation, ML, pentesting, and tool‑building.

One folder per project → one virtual environment inside it
This is the standard used by:

ML engineers

Backend developers

Cybersecurity tool authors

Automation engineers

Anyone who maintains multiple Python projects

And it solves every dependency problem you just ran into.

### Why is this structure ideal?
Each project gets its own isolated environment
Example:

Code
C:\Projects\gradio-test\venv
C:\Projects\automation-tool\venv
C:\Projects\ml-model\venv
Each one has:

its own Python version

its own pip

its own packages

zero interference with other projects

This means you can have:

Gradio running on Python 3.12

The first step is to download cursor

A pentesting tool running on Python 3.13

An ML model running on Python 3.11

All on the same machine, all clean.

### Step 1. Download cursor.
Cursor is an AI‑enhanced code editor built on top of VS Code that gives autonomous coding agents everything they need to work effectively on real software projects. It isn’t required to run AI agents, but it provides a uniquely structured environment where agents can read your entire codebase, make coordinated multi‑file edits, run terminal commands, and safely propose changes through diffs you can review. Because it handles context, indexing, guardrails, and execution in one place, Cursor becomes a practical home for agentic development—letting AI not just suggest code, but actually build, refactor, and debug features across your project in a controlled, reliable way.

www.cursor.com

During the installation, select the two options "Add open with cursor"

### Step 2. Deploy your file in a testing folder.

You will need to open this folder from the cursor IDE.

### Step 3. UV packet manager.
UV will automatically create and manage the virtual environment for you. UV will:

Detect your Python version

Create a .venv folder automatically

Install all dependencies from pyproject.toml

Pin versions and lock them in uv.lock

This is cleaner and faster than pip + venv.

Download the UV packet manager from: https://docs.astral.sh/uv

Verify the installation in PowerShell: uv --version

In the cursor IDE, open the terminal

Run the command "uv init"

Note: When creating this repository, I also had to download Python 3.12 from the official website.

After that, when I ran the command "py --list" in PowerShell, I saw both versions. 3.12 and 3.13.

We also need to specify what version of Python we will use and then we can syc:

uv python pin 3.12
uv sync

### Get a key from OpenAI

Got to the site https://platform.openai.com and got an API key.


Right-click to create a new file and name it ".env"

Add the line: OPENAI_API_KEY=sk-proj-1234567890 (Replace it with the KEY)

### We are ready to run our Jupyter Notebbok.

When running the cells cursor is going to ask us "select kernel".

Select Python Environments --> .venv

From here keep installing the libraries as nedded they will be automatically added to pyproject.toml

Examples (In Terminal):

uv add python-dotenv

uv add openai

uv add pypdf


