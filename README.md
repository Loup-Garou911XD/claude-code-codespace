# claude-code-codespace
A template repository to create and use claude code on codespace

# How to use
Just use this as template, and create a codespace
If you want to use it in an already working repository then follow the step by step installation process

## Step-by-Step Installation

### Step 1: Create Dev Container Configuration

In your blank repository, create the necessary directory and file.

Copy and paste this single command into your terminal:

```bash
mkdir -p .devcontainer && curl -o .devcontainer/devcontainer.json https://raw.githubusercontent.com/Loup-Garou911XD/claude-code-codespace/refs/heads/main/.devcontainer/devcontainer.json
```

### Step 2: Commit and Push Configuration
```bash
git add .devcontainer/devcontainer.json
git commit -m "Add Claude-Flow dev container configuration"
git push origin main
```

### Step 3: Rebuild Codespace
1. Press `Ctrl+Shift+P` (Command Palette)
2. Search for "Codespaces: Rebuild Container"
3. Select and confirm rebuild
4. Wait for container to rebuild with new configuration

### Step 4: Verify Installation
```bash
# Check Node.js
node --version

# Check Python
python --version

# Check Claude Code (command is 'claude', not 'claude-code')
claude --version

# Check Docker
docker --version
```

Expected output:
- Node.js: v22.17.1+
- Python: 3.11.2+
- Claude: 1.0.56+ (Claude Code)
- Docker: 28.3.2+

## Authenticate Claude
```bash
# Start Claude and authenticate
claude
```
- Complete the login process with your Anthropic account
- Choose subscription (default) or API key option
- After approval, you will land at http://localhost:42941/callback?code=...&state=...
- In local terminal, run `gh codespace ports forward 42941:42941 -c <codespace name>`
- Refresh the page and you will see confirmation for sign in
> [!NOTE]
> Change the port in gh cmd if its different for you in the localhost url

# Special thanks
This repo was created with the help of https://gist.github.com/raoulbia-ai/ec00967e8d9da4cfec22371655972acf 
