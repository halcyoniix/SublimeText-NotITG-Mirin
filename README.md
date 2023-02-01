# Sublime Text completions and syntax highlighting for NotITG and Mirin Template.
## THIS HAS MIRIN-SPECIFIC COMPLETIONS WHICH MAY GET IN THE WAY WHEN CODING IN NORMAL NOTITG ENVIRONMENTS.
Specifically the files `Mirin`, `Easings`, `Mods`, and `ActorTypes` all have completions relating to the Mirin Template. Feel free to edit these as you wish. (See PS at the bottom)

![](https://cdn.discordapp.com/attachments/978754506890313758/1070121981212622930/1.jpg)

## How to install
1. Nagivate to your Sublime Text package folder. To find it, open Sublime Text and use the command palette with `CTRL+SHIFT+P` and type `Browse Packages`. This should open the directory to your packages folder.
2. Extract the zip to the `User` folder. Create a `User` folder if there isn't one already. The full path after extraction should look like `<sublime_text_root>\Data\Packages\User\NotITG`.
3. Select the correct language via the syntax menu in the bottom right, stored in the `User` submenu. You can also use the command palette and typing `Set Syntax: NotITG`, which will show all available options.
4. (`OPTIONAL`) To get highlighting for methods and constants, go to the menu bar and select `Preferences > Customize Color Scheme` (or via the command palette), and copy these objects into the `rules` array.
	```json
	{
		"scope": "nitg.function",
		"foreground": "<COLOR>",
	},
	{
		"scope": "nitg.global",
		"foreground": "<COLOR>",
	},
	```
	Here's [Sublime Text color scheme documentation for style rules](https://www.sublimetext.com/docs/color_schemes.html#style-rules) if you need it.
	
A few extra things that could make your life easier:
- For a full list of all valid completions for a language, press `CTRL+SPACE`.
- If you'd like to write your own custom completions, here's [documentation for `.sublime-completions` files](https://www.sublimetext.com/docs/completions.html).
- Installing an extension like [ApplySyntax](https://packagecontrol.io/packages/ApplySyntax) to apply NotITG syntaxes only in specific directories. Here's an example of custom syntax rules that I use:
	```json
	"syntaxes": [
		{
			"syntax": "User/NotITG/NotITG Lua",
			"rules": [
				 {"file_path": ".*/(NotITG)/.*\\.lua$"},
			],
		},
		{
			"syntax": "User/NotITG/NotITG XML",
			"rules": [
				 {"file_path": ".*/(NotITG)/.*\\.xml$"},
			],
		},
		{
			"syntax": "User/NotITG/NotITG GLSL",
			"rules": [
				 {"file_path": ".*/(NotITG)/.*\\.frag$"},
				 {"file_path": ".*/(NotITG)/.*\\.vert$"},
			],
		},
	]
	```
	All `.lua`, `.xml`, `.frag`, and `.vert` files whose directory listing has "NotITG" in it will have the assigned NotITG Lua syntax automatically applied to it. This serves as a good timesave, as well as to not intrude on non-NotITG files that share the same extension but use different syntaxes.

PS: There's no official license for this, so feel free to edit any part of this as you please. Just credit me where credit is due. Thanks in advance.

-- halcyoniix