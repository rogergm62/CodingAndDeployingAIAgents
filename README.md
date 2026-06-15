# Coding And Deploying AI Agents
How to code and deploy AI Agents

Instructions:
- Create a folder to deploy this project
- This folder is important because we will create a virtual environment
- Clone this repo
- Download and install "cursor" IDE from the site: www.cursor.com (You can use the free version)
- During the installation, select the two options: Add "Open with Cursor" actions

- Once installed, Open Cursor
- Select Open Project and select the folder where the project is located
- Open the Window Editor and select the project.

- Download the uv package manager from https://docs.astral.sh/uv/
- Verify the installation in PowerShell by running: uv --version

- In cursor select view --> Terminal
- Run "uv sync" to synchronize the folder content
- After that, verify that file .venv was created.

- Get the OpenAI API keys.
- Go to https://platform.openai.com
- Log in or sign up
- Go to Settings --> Billing
- Add the minimum balance and no auto pay.
- Go to the API Keys section and create a new secret key.
- Copy the key to the clipboard.

- Go back to cursor and create a new file named ".env"
- Open that file and add: `OPENAI_API_KEY = YOUR KEY`
- If you are using another platform, follow the same method as follows:
- DEEPSEEK_API_KEY=
- GROQ_API_KEY=
