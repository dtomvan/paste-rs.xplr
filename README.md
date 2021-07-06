# paste.rs.xplr
Use this plugin to paste your files to [paste.rs](https://paste.rs/), and open/delete them later in fzf.

## Credit
I don't take any credit for this plugin, I ran [@sayanarijit](https://github.com/sayanarijit)'s yml-to-lua converter over his own xplr hack. 

## Requirements

- [fzf](https://github.com/junegunn/fzf)
- [sd](https://github.com/chmln/sd)
- [curl](https://github.com/curl/curl)


## Installation

- Add the following line in `~/.config/xplr/init.lua`

  ```lua
  package.path = os.getenv("HOME") .. '/.config/xplr/plugins/?/src/init.lua'
  ```

- Clone the plugin

  ```bash
  mkdir -p ~/.config/xplr/plugins

  git clone https://github.com/dtomvan/paste.rs.xplr ~/.config/xplr/plugins/paste-rs
  ```

- Require the module in `~/.config/xplr/init.lua`

  ```lua
  require("paste-rs").setup()
  
  -- Or
  
  require("paste-rs").setup{
    mode = "default",
    key = "P",
  }

  -- Type `Pp` and enjoy.
  ```


## Features

- Paste your files directly to paste.rs
- List all of your uploads (from the current session) and open them later.
- Delete your uploads (from the current session)
