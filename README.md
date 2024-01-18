# **KoPylot**: Your AI-Powered Kubernetes Assistant 🤖

[![Release](https://img.shields.io/github/v/release/avsthiago/kopylot)](https://img.shields.io/github/v/release/avsthiago/kopylot)
[![Build status](https://img.shields.io/github/actions/workflow/status/avsthiago/kopylot/main.yml?branch=main)](https://github.com/avsthiago/kopylot/actions/workflows/main.yml?query=branch%3Amain)
[![codecov](https://codecov.io/gh/avsthiago/kopylot/branch/main/graph/badge.svg)](https://codecov.io/gh/avsthiago/kopylot)
[![Commit activity](https://img.shields.io/github/commit-activity/m/avsthiago/kopylot)](https://img.shields.io/github/commit-activity/m/avsthiago/kopylot)
[![License](https://img.shields.io/github/license/avsthiago/kopylot)](https://img.shields.io/github/license/avsthiago/kopylot)

KoPylot is an open-source AI-powered Kubernetes assistant. Its goal is to help developers and DevOps engineers to easily manage and monitor their Kubernetes clusters. 

You can read more about the project in the [blog post](https://medium.com/@thiagoalves/introducing-kopylot-a-kubernetes-ai-assistant-264cff0e7846).

## 🤝 Note: 
This repo from https://github.com/avsthiago/kopylot with fixed text-davinci-003 has been deprecated. Origin author is Thiago Alves.

## 💫 Features:

- 🔍 **Audit**: Audit a resource, such as pods, deployments, or services using an LLM model.
![Audit](./resources/audit.png)

- 🩺 **Diagnose**: Diagnose resources, such as pods, deployments, or services using an LLM model.
![Diagnose](./resources/diagnose.png)

- 💬 **Chat**: Start a chat with KoPylot to generate kubectl commands based on your prompts.
![Chat](./resources/chat.png)

- ☸️ **Ctl**: A wrapper around kubectl. The arguments passed to the `ctl` subcommand are interpreted by kubectl.
![Ctl](./resources/ctl.png)


## 🚀 Quick Start:

1. Requests an API key from [OpenAI](https://help.openai.com/en/articles/4936850-where-do-i-find-my-secret-api-key).
2. Export the key using the following command:

```bash
export KOPYLOT_AUTH_TOKEN=your_api_key
```

NOTE: If you want to avoid having the key in your .bashrc, .oh-my-zsh/custom dir,
or your .bash_history or .zsh_history, a possible trick is to do something like this:

```bash
export KOPYLOT_AUTH_TOKEN=$(cat ../../../keys/openai)
```

3. Install KoPylot using pip:
```
pip install kopylot-gpt
```

4. Run KoPylot:
```
kopylot --help
```


## 📖 Usage:

```
Usage: kopylot [OPTIONS] COMMAND [ARGS]...                                           
                                                                                      
╭─ Options ──────────────────────────────────────────────────────────────────────────╮
│ --version                                                                          │
│ --install-completion        [bash|zsh|fish|powershell  Install completion for the  │
│                             |pwsh]                     specified shell.            │
│                                                        [default: None]             │
│ --show-completion           [bash|zsh|fish|powershell  Show completion for the     │
│                             |pwsh]                     specified shell, to copy it │
│                                                        or customize the            │
│                                                        installation.               │
│                                                        [default: None]             │
│ --help                                                 Show this message and exit. │
╰────────────────────────────────────────────────────────────────────────────────────╯
╭─ Commands ─────────────────────────────────────────────────────────────────────────╮
│ audit     Audit a pod, deployment, or service using an LLM model.                  │
│ chat      Start a chat with kopylot to generate kubectl commands based your        │
│           inputs.                                                                  │
│ ctl       A wrapper around kubectl. The arguments passed to the ctl subcommand are │
│           interpreted by kubectl.                                                  │
│ diagnose  Diagnose a resource e.g. pod, deployment, or service using an LLM model. │
╰────────────────────────────────────────────────────────────────────────────────────╯
```
