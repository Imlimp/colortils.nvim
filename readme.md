<div align="center">

<img src="res/colortils.svg" width=300>

# Colortils.nvim - Neovim color utils

</div>

<img src=https://user-images.githubusercontent.com/81827001/172016659-0543ca48-6080-4581-9b4f-ce35c1399138.gif width="500"/>


## ✨ Features
- Color picker with nice ui
- Some utilities for css colors
    - List Colors

## 📦 Installation and Usage

Use you favourite package manager and call the setup function.
```lua
use {
  "max397574/colortils.nvim",
  cmd = "Colortils",
  config = function()
    require("colortils").setup()
  end,
}
```

You can use the `Colortils` command to use this plugin.

#### Color picker
Use `Colortils picker` to access the color picker.
You can provide an optional argument which is the intial color the picker will have.
This is a hex color code without the `#` at the beginning (e.g. FF00AB).

You can use `h`/`l` to change the color value under the cursor.
With `<cr>` you can yank the hex color code into the register specified in settings (see defaults below).

#### Css Utilities
##### List colors
Use `:Colortils css list` to get a list of all the colors in a floating window.
This will *try* (**it's not a dependency**) to attach [nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua) ([maintained fork](https://github.com/xiyaowong/nvim-colorizer.lua)).

## ⚙️ Customization
You can change the settings by passing options to the setup function.
This is the default configuration:
```lua
require("colortils").setup({
    register="+", -- register in which color codes will be copied: any register
    color_preview =  "█ %s", -- preview for colors, if it contains `%s` this will be replaced with a hex color code of the color
    border = "rounded", -- border for the float
})
```

## 👀 Demo

#### Color Picker with "block"

![Screenshot 2022-05-30 at 20 02 39](https://user-images.githubusercontent.com/81827001/171042127-6b7fe7f3-a95e-4ce7-b1ea-8026d3c03805.png)


#### Color Picker with "hex"

![Screenshot 2022-05-30 at 20 03 40](https://user-images.githubusercontent.com/81827001/171042234-295e9bbf-d093-491c-98e8-c753f23f6dd1.png)

#### List css colors

![Screenshot 2022-05-31 at 18 56 23](https://user-images.githubusercontent.com/81827001/171230907-313fddc8-29e6-4b97-a842-8ea69ed5b6d5.png)
