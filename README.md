# TMUX Tutorial

## Contents

- [TMUX Tutorial](#tmux-tutorial)
  - [Contents](#contents)
  - [Introduction](#introduction)
  - [Basic TMUX Usage](#basic-tmux-usage)
  - [The tmux commands](#the-tmux-commands)



## Introduction

TMUX is a terminal multiplexer that allows you to split your terminal window into multiple panes, allowing you to run multiple terminal sessions within a single window. This can be particularly useful for managing multiple tasks or remote sessions from a single terminal window.

Go back to [Contents](#contents).



## Basic TMUX Usage

Here's a basic guide on how to use TMUX:

1. **Installation:** First, you need to make sure TMUX is installed on your system. You can typically install it using your system's package manager. 

Here's how to install TMUX on CentOS, Ubuntu, and macOS:

- CentOS:

You can install TMUX on CentOS using the yum package manager:

```bash
sudo yum install tmux
```

- Ubuntu:

You can install TMUX on Ubuntu using the apt package manager:

```bash
sudo apt-get update
sudo apt-get install tmux
```

- macOS:
  
You can install TMUX on macOS using the Homebrew package manager:

```bash
brew install tmux
```

2. **Starting TMUX:** You can start TMUX by simply typing `tmux` in your terminal and pressing Enter. This will open a new session within the TMUX environment.

3. **Basic Commands:**

   - **Creating Panes:** Once inside TMUX, you can create multiple panes by using the shortcut `Ctrl + b` followed by `%` to split the current pane vertically, or `Ctrl + b` followed by `"` to split the current pane horizontally.

   - **Navigating Panes:** You can switch between panes using `Ctrl + b` followed by an arrow key (`←`, `→`, `↑`, `↓`).

   - **Closing Panes**: To close a pane, simply exit the terminal session running within it (`exit` or `Ctrl + d`).

   - **Creating Windows:** Apart from panes, you can create multiple windows within a TMUX session. Press `Ctrl + b` followed by `c` to create a new window.

   - **Switching Windows:** You can switch between windows using `Ctrl + b` followed by a number corresponding to the window number.

   - **Exiting TMUX:** To exit TMUX, you can simply close all windows and panes within it, or you can detach from the session by pressing `Ctrl + b` followed by `d`. This will leave your TMUX session running in the background, and you can reattach to it later using tmux attach.

4. **Customization:** TMUX is highly customizable. You can customize the key bindings, appearance, and behavior according to your preferences. The configuration file for TMUX is typically located at `~/.tmux.conf`.

These are just the basic commands to get started with TMUX. As you become more familiar with it, you can explore more advanced features such as session management, window management, synchronization between panes, and more. The `tmux` command also has a rich set of options and subcommands, which you can explore further by checking its documentation (`man tmux`).

Go back to [Contents](#contents).



## The tmux commands

Here's a comprehensive list of TMUX commands along with their descriptions:

1. **Session Management:**
  - `tmux new-session [-d] [-s session-name]` - Create a new TMUX session.
  - `tmux attach-session [-t target-session]` - Attach to an existing TMUX session.
  - `tmux switch-client [-t target-session]` - Switch to another client (another terminal) attached to the same session.
  - `tmux detach [-s target-session]` - Detach the current client from the session.
  - `tmux list-sessions` - List all TMUX sessions.
  - `tmux kill-session -t <session-name>` - Kill a specific TMUX session using its name.
  - `tmux kill-session -t <session-number>` - Kill a specific TMUX session using its number.
  - `tmux kill-session -a` - Kill all sessions except the current one.
    - The `-a` option specifies to kill all sessions.

Go back to [Contents](#contents).



2. **Window Management:**
   - `Ctrl + b c` - Create a new window.
   - `Ctrl + b ,` - Rename the current window.
   - `Ctrl + b w` - List all windows.
   - `Ctrl + b n` - Move to the next window.
   - `Ctrl + b p` - Move to the previous window.
   - `Ctrl + b &` - Close the current window.
   - `Ctrl + b <number>` - Switch to window number <number>.

Go back to [Contents](#contents).



3. **Pane Management:**
   - `Ctrl + b %` - Split the current pane horizontally.
   - `Ctrl + b "` - Split the current pane vertically.
   - `Ctrl + b o` - Move to the next pane.
   - `Ctrl + b ;` - Move to the previously active pane.
   - `Ctrl + b x` - Close the current pane.
   - `Ctrl + b q` - Show pane numbers, then type the number to move to that pane.
   - `Ctrl + b {` - Move the current pane to the left.
   - `Ctrl + b }` - Move the current pane to the right.
   - `Ctrl + b z` - Toggle pane zoom (maximize/minimize).
   - `Ctrl + b Ctrl + <arrow>` - Resize the current pane in the direction of `<arrow>`.

Go back to [Contents](#contents).



4. **Copying and Scrolling:**
   - `Ctrl + b [` - Enter copy mode to scroll through the buffer (press q to exit copy mode).
   - `Ctrl + b PgUp/PgDn` - Scroll up/down in copy mode.
   - `Ctrl + b ]` - Paste the copied text.

Go back to [Contents](#contents).



5. **Other Commands:**
   - `Ctrl + b d` - Detach the current client from the session.
   - `Ctrl + b :` - Enter TMUX command prompt to enter various commands (e.g., rename-session, set-option, etc.).
   - `Ctrl + b ?` - Show key bindings help.

Go back to [Contents](#contents).



These are the basic TMUX commands to get you started. You can explore further by reading the TMUX manual (man tmux) or by typing tmux followed by `Ctrl + b ?` to see a list of key bindings within TMUX.

Go back to [Contents](#contents).
