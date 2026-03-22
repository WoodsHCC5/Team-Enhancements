# 🚀 Claude Code + GitHub Copilot Setup Guide

A comprehensive guide to connecting Claude Code with GitHub Copilot for enhanced AI-powered development.

## 🎯 Our Goal

**We're not here to replace software engineers and architects – we're here to make them more effective.** This setup leverages GStack (a powerful development workflow toolkit) combined with your existing GitHub Copilot license to supercharge your development process. Think of it as giving your development team AI-powered superpowers while keeping human creativity and decision-making at the center.

### What Makes GStack So Powerful?

- **🔍 Intelligent Code Exploration**: Quickly understand large codebases with smart search and analysis
- **🏗️ Architectural Planning**: Get structured implementation plans before you start coding
- **🧪 Automated QA Testing**: Comprehensive testing workflows that catch issues early
- **📝 Smart Documentation**: Auto-generate and maintain project documentation
- **🚀 Streamlined Deployment**: One-command workflows for shipping code with confidence
- **🔄 Development Lifecycle Management**: From brainstorming to retrospectives, all in one toolkit
- **🎨 Design System Integration**: Maintain visual consistency across your applications
- **📊 Code Quality Analysis**: Built-in review processes and quality gates

**Learn more about GStack**: https://github.com/garrytan/gstack

## 📋 Prerequisites

Make sure you're running this setup on a WSL instance or Linux environment with a valid GitHub Copilot license.

## 🔧 Installation Steps

### 1. Install System Dependencies

First, install the required system packages:

```bash
sudo apt update && sudo apt install unzip
```

### 2. Install Node.js

Ensure you have Node.js 18+ installed on your WSL instance. You can use nvm or install directly from the official repository.

### 3. Install Claude Code CLI

```bash
npm install -g @anthropic-ai/claude-code
```

### 4. Install Bun

Install Bun package manager (requires unzip):

```bash
curl -fsSL https://bun.sh/install | bash
```

### 5. Install GStack Skills

Clone and set up the GStack skills package:

```bash
git clone https://github.com/garrytan/gstack.git ~/.claude/skills/gstack && cd ~/.claude/skills/gstack && ./setup
```

### 6. Install Copilot API Bridge

Install the Copilot API bridge to connect Claude Code with your GitHub Copilot license:

```bash
npm install -g copilot-api
```

### 7. Configure Environment Variables

Add the following lines to your `~/.bashrc` file:

```bash
export CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1
export ANTHROPIC_BASE_URL="http://localhost:4141/v1"
export ANTHROPIC_API_KEY="any-string"
```

After adding these lines, reload your bash configuration:

```bash
source ~/.bashrc
```

## 🎯 Starting Claude Code

### Launch the Services

1. **Start Copilot API Bridge**: Open a new terminal and the copilot-api service will start automatically when Claude connects
2. **Launch Claude**: In another terminal, run:

```bash
claude
```

## ✅ Verification

Once setup is complete, you should be able to:

1. ✅ Run `claude` command successfully
2. ✅ Connect to GitHub Copilot through the API bridge
3. ✅ Use GStack skills for enhanced functionality
4. ✅ Enjoy AI-powered coding with your existing Copilot license

## 🆘 Need Help?

If you encounter issues during setup:

1. Ensure all dependencies are properly installed
2. Check that environment variables are correctly set in `.bashrc`
3. Verify your GitHub Copilot license is active
4. Restart your terminal session after modifying `.bashrc`
5. Make sure the copilot-api service is running on port 4141

## 💡 Why This Setup?

This configuration allows you to:
- **Leverage your existing GitHub Copilot subscription** instead of paying for separate API access
- **Use Claude Code's advanced features** with familiar AI assistance
- **Access GStack skills** for enhanced development workflows
- **Work entirely within your WSL environment** for consistent tooling

---

**Happy coding with Claude + Copilot! 🎉**
