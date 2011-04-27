This bundle is a modified version of the Lua bundle for TextMate which contains support. It contains support for the libraries I use most in Lua. These are listed in the following sections. I've also modified a number of things in it to conform to the way I like it.

## [LÖVE](http://love2d.org) game engine

Features include:

* Highlighting for Love modules, classes, functions and enums.
* Run the game. If you're editing in a project, focus can be on any file, otherwise you must execute this on the main.lua or any other top level file. Shortcut is Command+R.
* Build a .love file. Same rules apply for file focus as running the game. This command will place a file called "game.love" in your project folder. Shortcut is Command+B.
* Look up phrase on the Love2D wiki. For example, highlight "love.physics" in TextMate, execute the command and you'll be taken to wiki page for the module in your browser.
* Search phrase(s) on the Love2D forums. Highlight the keywords you want to search in TextMate and execute the command.
* Snippets for the love.* callbacks.

This is all contained in a separate scope, named `source.lua.love`.

## [MiddleClass](http://github.com/kikito/middleclass)

Current features for this are three snippets:

* One really handy one for declaring a class.
* One for defining a method (this can be used outside of MiddleClass).
* One for making a mixin.

## [Telescope](http://github.com/norman/telescope)

Lots of snippets for this one! It has snippets for...

* All the `assert_*` and `assert_not_*` functions (except for `assert_less_than`, `assert_greater_than` and those types - as I think those are better done by using stuff like `assert_true(x < y)`).
* `before`, `setup`, `after`, and `teardown`.
* `context` and `describe`.
* `test`, `it`, and `should`.

Enjoy!
