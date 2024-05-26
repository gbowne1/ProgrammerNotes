# tmux

## Installing tmux

sudo apt install tmux

Check the version of tmux with `tmux -V`

There is a configuration file used. It is `~/.tmux.conf`

there is documentation at `man tmux`.

The github is at <https://github.com/tmux/tmux>

Systemwide configruation is at `/etc/tmux.conf`

## shell flags used with tmux

used with `tmux`, these flags return results:

-c requires an argument
-d ?
-f requires an argument
-l starts tmux
-q starts tmux
-u starts tmux
-v starts tmux

## tmux commands

tmux comes with a comprehensive set of built-in commands for various purposes. These commands are typically prefixed with the configured prefix key (default: Ctrl + b) followed by a single key. Here are some common examples:

- Session Management
        `new-session` Creates a new tmux session.
        `attach` Reattaches to a detached session.
        `list-sessions` Lists all active sessions.
        `kill-session` Terminates a tmux session.
- Window Management
        `new-window` Creates a new window within the current session.
        `select-window` Selects a specific window.
        `close-window` Closes the current window.
        `rename-window` Renames the current window.
- Pane Management`
        `split-window` Splits the current window horizontally or vertically.
        `select-pane` Selects a specific pane within the window.
        `close-pane` Closes the current pane.
        `swap-pane` Swaps the positions of two panes

Here's a glimpse into working within tmux

 Splitting Panes
    Use Ctrl + b followed by % (horizontal split) or " (vertical split) to create new panes within a window.

 Switching Panes
    Navigate between panes using arrow keys prefixed with Ctrl + b.

 Copying and Pasting:
    Tmux offers built-in copy and paste functionality. You can typically select text within
    a pane using the mouse and copy it using Ctrl + b followed by c. Pasting can be done with Ctrl + b followed by p.

 Detaching and Reattaching:
    Detach from a session using Ctrl + b followed by d. Reattach to a detached session using the tmux attach command.

Tmux offers a vast array of options for customization, allowing you to tailor its behavior to your preferences. Here's a breakdown of the different categories of options:

Server Options:

These options affect the global tmux server and apply to all sessions by default. You can set them using the set-option -s command. Some common server options include:

    set-option -s default-shell: Defines the default shell launched within tmux sessions.
    set-option -s mouse on: Enables mouse support for interacting with panes and windows.

Session Options:

These options configure specific tmux sessions. You can set them using set-option without the -s flag while within a session or define them in your configuration file (~/.tmux.conf). Session options can override server options for specific sessions. Examples include:

    set-option -g status-bg colour232: Sets the background color of the status bar for the current session.
    set-option window-name "coding": Sets the name of the current window.

Window Options:

Window options control the behavior of individual windows within a session. Use set-option -w to configure them. Here are some examples:

    set-option -w automatic-rename on: Automatically assigns names to newly created windows.
    set-option -w aggressive-resize on: Enables more aggressive window resizing when using keyboard shortcuts.

Pane Options:

These options affect individual panes within windows. You can set them using set-option -p. Examples include:

    set-option -p mode-keys vi: Sets the key bindings within the pane to vi mode for navigation and editing.
    set-option -p scroll-keys emacs: Sets the key bindings for scrolling within the pane to emacs mode.

Show drafts

Tmux relies on a prefix key combination followed by specific keys to execute commands and navigate within the terminal workspace. By default, the prefix key is Ctrl + b. However, you can customize this in your tmux configuration file (~/.tmux.conf).

Here's a glimpse into some essential tmux keyboard shortcuts:

Session Management:

    Ctrl + b + s: Create a new session.
    Ctrl + b + d: Detach from the current session (background execution).
    tmux attach: Reattach to a detached session.
    Ctrl + b + l: List all active sessions.
    Ctrl + b + kill-session: Terminate the current session.

Window Management:

    Ctrl + b + c: Create a new window within the current session.
    Ctrl + b + n: Select the next window.
    Ctrl + b + p: Select the previous window.
    Ctrl + b + w: Rename the current window.
    Ctrl + b + x: Close the current window.

Pane Management:

    Ctrl + b + %: Split the window horizontally into two panes.
    Ctrl + b + ": Split the window vertically into two panes.
    Ctrl + b + Arrow Keys: Navigate between panes (Up, Down, Left, Right).
    Ctrl + b + x: Close the current pane.

Other Essential Shortcuts:

    Ctrl + b + [: Enter copy mode for copying text within panes.
    Ctrl + b + ]: Paste previously copied text.
    Ctrl + b + q: Exit tmux completely (detaching all sessions)
