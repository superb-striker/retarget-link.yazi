# retarget-link.yazi

A Yazi plugin for interactively changing the target of a symlink.

https://github.com/user-attachments/assets/4ccecbb6-38cc-4975-b138-41ace2a7ffc0

## Features

- Opens an input prompt directly beneath the hovered symlink.
- Prefills the prompt with the symlink's current target.
- Accepts relative and absolute targets.
- Leaves the symlink unchanged when the prompt is cancelled.

## Installation

Install the plugin with Yazi's package manager:

```sh
ya pkg add superb-striker/retarget-link
```

## Usage

Add a keybinding to `~/.config/yazi/keymap.toml`:

```toml
[[mgr.prepend_keymap]]
on   = [ "g", "r" ]
run  = "plugin retarget-link"
desc = "Change symlink target"
```

Hover over a symlink and press `g` followed by `r`. Edit the target and press
Enter to apply it, or press Esc to cancel. You can replace the example keys
with any binding you prefer.

## Requirements

- Yazi 25.5.31 or newer when installing with `ya pkg`.
- A Unix-like system with `readlink` and `ln` available.

The plugin has been tested with Yazi 26.9.1.

## License

[MIT](LICENSE)
