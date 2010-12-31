This bundle is a modified version of the Lua bundle for TextMate which contains support for the [Love](http://love2d.org) 0.7.0 game engine. Features include:

* Highlighting for Love modules, classes, functions and enums.
* Look up phrase on the Love wiki. For example, highlight "love.physics" in TextMate, execute the command and you'll be taken to wiki page for the module in your browser.
* Search phrase(s) on the Love forums. Highlight the keywords you want to search in TextMate and execute the command.
* Run the game. If you're editing in a project, focus can be on any file, otherwise you must execute this on the main.lua or any other top level file. Shortcut is Command+R.
* Build a .love file. Same rules apply for file focus as running the game. This command will place a file called "game.love" in your project folder. Shortcut is Command+B.

Enjoy!

# Completion Contribution

Currently what's being worked on is the tedious task of adding completions for all functions. If you would like help complete this (that would really be appreciated), here's what you need to know.

The you'll need to edit is Support/completion.rb. In this file is an array of choices that can show up in the completions box. Each item can contain three keys:

* d - This is where the full function name goes. For example "love.filesystem.isFile".
* t - This is what shows up in the tooltip when the user selects a function. This will contain a description of the function and it's parameters.
* i - This is what is inserted after the function name. As well as the parenthesis this contains all parameter names separated by commas.

## Grouping

Here's how the completion items should be grouped. The first item (and group) should be the 'love.' item, then come the callbacks, and then a group for each module ordered alphabetically. At the top of each module group should be an item with just the module name with a '.' appended; for example, 'love.graphics.'.

## Tooltips

The tooltip key should first contain a short description of the function or module copied directory from the wiki. If it is a function, then a &lt;br&gt; tag should follow. This should be followed each parameter listed out with it's type and description. It should look like this:

<pre>Description.&lt;br&gt;&lt;strong&gt;param1&lt;/strong&gt; = param1 description.&lt;br&gt;&lt;strong&gt;param2&lt;/strong&gt; = param2 description.</pre>

## Insertions

Insertions should contain parenthesis with a list of the parameters inside them. It should look like this:

<pre>(param1, param2)</pre>

For consistency, don't use space after or before parenthesis.