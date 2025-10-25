# Compose for Notepad++

**Compose for Notepad++** is a plugin for [Notepad++](https://github.com/notepad-plus-plus/notepad-plus-plus) which implements a [compose key](https://en.wikipedia.org/wiki/Compose_key) for entering characters that are not available on the keyboard.

Like Notepad++, this software is released under the GNU General Public License (either version 3 of the License, or, at your option, any later version). Some original source code files which are not dependent on Notepad++ are released under the [MIT (Expat) License](https://www.opensource.org/licenses/MIT): see individual files for details.

This plugin uses [JSON for Modern C++](https://github.com/nlohmann/json) by Niels Lohmann (https://nlohmann.me), which is released under the [MIT License](https://www.opensource.org/licenses/MIT).

## Purpose

A [compose key](https://en.wikipedia.org/wiki/Compose_key) is a key that indicates the following keys are to be interpreted in a special way. Usually an easy-to-remember sequence produces a character that’s not on the keyboard, such as `'a` for `á` or `---` for an em-dash. **Compose for Notepad++** brings this facility to Notepad++ in a flexible and customizable way, without affecting how you type when using any other software on your computer.

## Features

When **Compose for Notepad++** is first used, the compose key is not enabled. You can toggle that using the first item on the plugin’s menu, and the enabled or disabled state will be remembered.

**Compose** does nothing until you press the key or key combination chosen as the Compose key; then it watches the characters you type next. When it recognizes a meaningful sequence it substitutes the characters defined for that sequence — usually entering a special character that isn’t available on your keyboard. Examples:

- *Compose* `AE` types `Æ`.
- *Compose* `-L` types `£`.
- *Compose* `.-a` types `ǡ`.

Pressing the Compose key twice does whatever that key or key combination did originally.

When enabled, **Compose for Notepad++** takes effect anywhere you press the Compose key in **Notepad++**. You can use compose key sequences in dialogs such as **Find** and **Replace**, or even in plugin dialogs, as well as when editing text.

You can select almost any key or key combination as the Compose key using the **Compose key...** item on the menu. The default Compose key is the **Insert** key (without **Alt**, **Ctrl** or **Shift**). Another good choice would be the **Caps Lock** key, if you don’t use that key often. You can also choose a typical “shortcut-style” key combination, such as **Ctrl+Alt+P**.

Since **Compose for Notepad++** works at the application level, you can use compose key sequences in dialogs such as **Find** and **Replace**, or even in plugin dialogs, as well as when editing text.

A [long list of pre-defined sequences](https://coises.github.io/Compose-for-NotepadPlusPlus/help.htm#predeflist) is provided. You can specify additional sequences in a user definitions file. You could use this feature to define sequences for special characters you want that are not in the pre-defined set; but since the inserted text is not limited to a single character, you could also create shorthand sequences for any text you want to insert with just a few keystrokes.

The pre-defined sequences include all the HTML named character entities; for example, you can type *Compose* `&copy;` to type the copyright symbol. You can also enter *Compose* `&#...;` and *Compose* `&#x....;` sequences, or just type the Compose key, the hexadecimal value of a Unicode code point, and the Enter key. (If the hexadecimal value begins with two letters, type a zero first to be sure you don’t trigger a different, pre-defined sequence.)

Around thirty combining marks (accents) are defined. You can enter sequences using multiple marks, such as `[ComposeKey].-a` to type `ǡ` (lower case `a` with a dot above and a macron). **Compose for Notepad++** will insert a pre-composed Unicode character when one exists; otherwise it will insert the appropriate combining characters.

A detailed [help file](https://coises.github.io/Compose-for-NotepadPlusPlus/help.htm) is available.

## Installation

This plugin is not yet available through Notepad++ Plugins Admin.

To install **Compose for Notepad++**, download the x86 or x64 zip file, depending on whether you're using 32-bit or 64-bit Notepad++, from the [latest release](https://github.com/Coises/Compose-for-NotepadPlusPlus/releases/latest/). Unzip the file to a folder named **Compose** (the name must be exactly this, or Notepad++ will not load the plugin) and copy that folder into the plugins directory where Notepad++ is installed (usually **C:\Program Files (x86)\Notepad++\plugins** for 32-bit versions or **C:\Program Files\Notepad++\plugins** for 64-bit versions).

