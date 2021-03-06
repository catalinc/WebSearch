# WebSearch

**It will no longer be updated. If someone wants to keep updating it, contact me.**

[Sublime Text](https://www.sublimetext.com) plugin to search on World Wide Web.

This package adds:

* A `Web Search` command to the context menu on the view.
* A command palette for the current selection or word
* A command palette that will ask you what to search
* A command palette for change engine during session (Close Sublime Text, return to active engine)

By default Google is used for web searches, but the search engine is configurable.

# Installation

Using [Package Control](http://wbond.net/sublime_packages/package_control)

- From command palette `Package Control: Install Package`
- Look for "WebSearch"

## Usage

- Using context menu on view, see `context_menu` options for customize.
- Place the cursor inside a word or select some text and press `Ctrl+Shift+s`.
- Using Command Pallete:
  Find WebSearch... and select available options

# Settings

    {
        // Select current engine
        "current_engine": "Google",
        // Default engines defined inside of plugin
        // is possible overwritte any engine using same name
        // "engines":
        // {
        //     "Ask": "https://www.ask.com/web?q=",
        //     "Bing": "https://www.bing.com/search?q=",
        //     "DuckDuckGo": "https://duckduckgo.com/?q=",
        //     "Google": "https://google.com/search?q=",
        //     "Wikipedia": "https://wikipedia.org/w/index.php?search=",
        //     "Yahoo": "https://search.yahoo.com/search?p="
        // },
        "engines": {},
        // Enable developer engines
        "use_developer_engines": false,
        // Default developer enfines inside of plugin
        // is possible overwritte any engine using same name.
        // They are the ones that have occurred to me ;)
        // "developer_engines":
        // {
        //     "MDN": "https://developer.mozilla.org/search?q=",
        //     "PHP": "https://php.net/search.php?show=quickref&pattern=",
        //     "Python": "https://docs.python.org/3/search.html?q=",
        //     "Python2": "https://docs.python.org/2/search.html?q=",
        //     "WordPress": "https://developer.wordpress.org/?s="
        // },
        "developer_engines": {},
        // Exclude available engines for show
        // Default to exclude: ["Ask", "Bing", "Yahoo", "Python2"]
        "exclude_engines_from_list": ["Ask", "Bing", "Yahoo", "Python2"],
        // Change mode of the context menu
        "context_menu_with_children": false,
        // Show context menu with different caption:
        // 1 - default text caption "Web Search" (disabled if "context_menu_with_children": true)
        // 2 - Custom text "Search on <engine>"
        // 3 - Custom text with excerpt "Search on <engine> for <excerpt>..."
        "context_menu_description": 3,
        // Length of the selected text for view in context menu
        "context_menu_description_length": 10,
        // Mode to open browser, tab or window
        "browser_mode": "tab",
        // Select and change the search engine when the Command Palette is used
        // Command palette option on execute:
        // - WebSearch: Search selected text
        // - WebSearch: Search text
        // Note:
        // It does change globally, to maintain the "current_engine" and not have to change it again.
        "engine_change": false,
        // Add "WebSearch: <engine>" on status bar
        "show_current_engine_on_status_bar": true,
        // Use for remove or change status bar text prefix
        "status_bar_text_prefix": "WebSearch:"
    }



### Add a new or rewritte exists search engine

- Open `Preferences > Package Settings > Web Search > Settings - User`
- Add a new entry under `engines`

Code:

    {
        "engines": {
            "EngineName": "EngineUrl"
        }
    }


### Available keyboard shortcut

- For launch search with current engine `ctrl+shift+s`
- For launch search with custom query `ctrl+alt+s`
- For change current engine only on current session `ctrl+shift+e`

### Change default keyboard shortcut

Open `Preferences > Package Settings > Web Search > Key Bindings - User`
