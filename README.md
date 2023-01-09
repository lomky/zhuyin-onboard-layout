
# Zhuyin (Bopomofo) keyboard layout for the Onboard virtual keyboard.

A zhuyin keyboard for [Onboard](https://launchpad.net/onboard), the virtual on screen keyboard for linux.

I have found Onboard to be the best onscreen keyboard for use in combination with [i3wm](https://i3wm.org/), and needed access to the [Zhuyin Fuhao](https://simple.wikipedia.org/wiki/Zhuyin) to assist with learning Taiwanese Mandarin & Traditional Chinese characters.

I have not created number or punctuation layers, but would welcome that contribution.

This repo was only possible because of the repo created by @EricGebhart [onboard-layouts](https://github.com/EricGebhart/onboard-layouts).

## Installing these keyboard layouts.

Requires [Onboard](https://launchpad.net/onboard), available through your package manager.

- clone this repo,
- `ln -s /path/to/repo/zhuyin.onboard ~/.local/share/onboard/layouts/`
- `ln -s /path/to/repo/zhuyin-Alpha.svg ~/.local/share/onboard/layouts/`
- `onboard -l zhuyin`

## Editing, or creating your own layouts

- Open the onboard-settings and copy the layout you are interested in
- Open both files in your favorite editor.
- To change the keys, you only need to edit the `.onboard` file:
  - Locate the key you want to change in the SVG's XML, note its `id`
  - Find the `key` with that `id `in the `.onboard` file, leave the `id` unchanged.
  - Add the fields `char="ㄚ" label="ㄚ"`, putting your character in place of the `ㄚ`
- To tweak the layout of the keys:
  - Open the SVG; find the `rect` tag you want to change, or create a new one alongside the existing `rect` tags.
  - Set the `x` and `y` to the top left corner of where you want the key to appear
  - Set the `width` adn `height` to your desired values
  - Copy the style from another key that matches the appearance you want
  - Ensure the `rect` has a unique `id`
  - If you created a new `rect`:
    - Open the `.onboard` file
    - Copy a new `key` alongside the other `key`s
    - Set the `id` to your new `id` from the SVG
    - Set the `char` and `label` as instructed above

## Onboard documentation

There is an HTML version of the Onboard documentation in the doc directory of this repo. Point your browser at the repository's `/doc/index.html` file to browse it.
