# Scroll Faster
Visual Studio Code extension "scroll-faster" allows you to scroll the editor up and down faster, by "x" number of lines using keybindings, where "x" can be user defined.  
This overrides the keybindings for the default "scrollLineUp" and "scrollLineDown" binded to "Ctrl+UpArrow/DownArrow" (windows) to allow the same action with the same keybindings but just 'faster'.  

## Features
- Scroll editor multiple lines at once using the same scroll keybindings.
- Custom line numbers to scroll by through the "set scroll lines by..." setting from command palette or user settings.
- Optional cursor follow feature, where cursor can be set to follow along the scroll at the edge of the view port instead of being left behind at original position by default
- Allow reverse scrolling by setting the number of lines to scroll the editor on every scroll to a negative number
- Extension activated on vscode startup using the "*" activation event.

## Requirements
<!-- If you have any requirements or dependencies, add a section describing those and how to install and configure them. -->
-- NIL --

## Extension Settings
Any VS Code settings through the `contributes.configuration` extension point.  
This extension contributes the following settings:
* `scroll-faster.scrollByLines`: Number of lines to scroll the editor by on every scroll command
* `scroll-faster.cursorFollowsScroll`: Should cursor follow along as editor scrolls?

## Known Issues
<!-- Calling out known issues can help limit users opening duplicate issues against your extension. -->
- Not exactly an issue, but user's should take note that, this extension Overrides keybindings of default line by line scrolling

## License, Author and Contributing
This project is developed and made available under the "MIT License". Feel free to use it however you like and contribute changes to build on top of it!  
If you have any questions, contact us via via at tech@enkeldigital.com  
Authors:
- [JJ](https://github.com/Jaimeloeuf)

## Roadmap
- [ ] Smooth scrolling instead of immediate viewport jump/reveals which will be extremely helpful for scrolling past large amount of lines
- [ ] Allow half viewport up/down scrolls instead of absolute number of lines to scroll by

## Release Notes
### 0.2.2
- Added extra check for NaN inputs for "scroll by lines" value

### 0.2.1
- Added command to set the optional cursor follow feature

### 0.2.0
- New optional cursor follow feature, where cursor follows along the scroll instead of being left behind at original position by default

### 0.1.3
- Optimized reads to configuration, to use a cached value and only update the cache value when configuration is changed.

### 0.1.2
- Minor bug fix for bad keybinding

### 0.1.1
- Minor bug fix to upgrade vs code engine version
- Cleaned up logging code to make it more discreet.
- Added new npm script for vsce publishing workflow

### 0.1.0
Initial release with basic fast scrolling and scrollByLines setting.
