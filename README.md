# Tmux Configuration Setup

This guide will walk you through the process of setting up a custom Tmux configuration and plugins from a GitHub repository. Follow the steps below to clone the repository, set the custom configuration file path, and load the plugins.

## Step-by-Step Instructions

1. **Clone the Repository:**
   First, clone the Tmux configuration repository into your `.config/tmux` directory.
   ```bash
   git clone https://github.com/uygunbodur/tmuxv2.git ~/.config/tmux

2. **Set Up an Alias for Tmux:**
   To make Tmux use the custom configuration file by default, create an alias in your shell configuration files (.bashrc and .zshrc).

   For bash:
```bash
echo "alias tmux='tmux -f ~/.config/tmux/tmux.conf'" >> ~/.bashrc
```

For zsh:
```bash
echo "alias tmux='tmux -f ~/.config/tmux/tmux.conf'" >> ~/.zshrc
```

3. **Reload the Shell Configuration:**
Apply the changes by sourcing the shell configuration files.

```bash
source ~/.bashrc
source ~/.zshrc
```

4.	**Restart Tmux:**
Kill any running Tmux server to ensure the new configuration is loaded.

```bash
tmux kill-server
```

5. **Start Tmux:**
Start a new Tmux session, which will now use the custom configuration file.
```bash
tmux -f ~/.config/tmux/tmux.conf
```

6. **Install Plugins:**
If the repository includes plugins managed by Tmux Plugin Manager (TPM), press the following key combination inside Tmux to install the plugins.
```bash
prefix + I
```
