# talosctl-variables

Zsh helper that sets up persistent KUBECONFIG and TALOSCONFIG environment variables for talosctl and kubectl, so you don't have to export them manually in every new terminal session.

## What it does

Prompts for the path to your Talos config directory, then writes a small env file at ~/.config/talos-env.sh pointing KUBECONFIG and TALOSCONFIG at that directory. It then adds a source line for that file to ~/.zshrc if one isn't already present, so the variables persist across terminal sessions and restarts.

## Usage

Run the script and enter the full path to your Talos config directory when prompted, for example /Users/you/.talos. Then reload your shell with source ~/.zshrc or open a new terminal.

## Requirements

Zsh. Assumes a Talos config directory containing a kubeconfig file and a talosconfig file.
