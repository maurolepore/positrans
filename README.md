
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Approaching Positron from VS Code for R

> As someone working with R and used to VS Code (or RStudio), I want to
> know how to transition to Positron smoothly, so that I can more easily
> collaborate with colleagues comming from RStudio (or VS Code).

Positron is a polyglot IDE with great support for R. Because it’s
similar in many ways to both VS Code and RStudio, it’s an excellent
meeting point for those comming from either IDE. However, Positron is
also different in many ways to both VS Code and RStudio, so the
transition will come with some pain.

To reduce that pain and stay productive, you can taste Positron or start
preparing for the transition with relatively small and few changes to
your current workflow from the comfort of your favorite IDE.

## Positron

[Positron](https://positron.posit.co/) includes:

- Tools for data science:
  - R console
  - Ability to send R code from scripts to the console with ctrl+enter.
  - Panels to explore plots and data.
  - Support for Quarto
- Tools for software development:
  - Keyboard shortcuts for building R packages with devtools
  - Support for Shiny
  - Testing
- Tools for debugging R code.

You can enable [RSdudio keyboard
shortcuts](https://positron.posit.co/keyboard-shortcuts.html#rstudio-keymap),
e.g.:

- Send code to the R console: ctrl+enter
- Restart R: ctrl+shift+0
- Assign `<-`: alt+-
- Pipe `|>`: ctrl+M
- Develop R packages using the devtools workflow:
  - `load_all()`: ctrl+shift+L
  - `test()`: ctrl+shift+T
  - `document()`: ctrl+shift+D
  - `check()`: ctrl+shift+E

## VS Code

[Visual Studio Code](https://code.visualstudio.com/) comes with little
support for R, but these few extensios and keyboard shortcuts
approximate Positron’s experience for R.

- Extensions:

<!-- -->

    # Basic R support, e.g. send code to the R console with Ctrl+Enter 
    code --install-extension reditorsupport.r
    # Needs this R package
    Rscript -e 'install.packages("languageserver")'

    # Debug
    code --install-extension rdebugger.r-debugger

    # Test
    code --install-extension hbenl.vscode-test-explorer
    code --install-extension meakbiyik.vscode-r-test-adapter

    # Shiny
    code --install-extension posit.shiny

    # Quarto
    code --install-extension quarto.quarto

TODO: In VSCode command pallete run `r.debugger.updateRPackage`

- Shortcuts: Place your key bindings in this file to override the
  defaults: ~/.config/Code/User/keybindings.json

``` json
[
  // BASIC R SUPPORT
    {
        // Create a new R terminal (similar to restarting R)
        "key": "ctrl+shift+0",
        "command": "r.createRTerm"
    },
    {
        // Assign
        "key": "alt+-",
        "command": "type",
        "args": { "text": " <- " },
        "when": "editorTextFocus && editorLangId == 'r'"
    },
    {
        // Pipe
        "key": "ctrl+shift+m",
        "command": "type",
        "args": { "text": " |> " },
        "when": "editorTextFocus && editorLangId == 'r'"
    },
    
    // R PACKAGE DEVELOPMENT WITH DEVTOOLS
    {          
        "key": "ctrl+shift+l",
        "command": "r.loadAll"
    },
    {
        "key": "ctrl+shift+e",
        "command": "r.check"
    },
    {
        "key": "ctrl+shift+d",
        "command": "r.document"
    },
    {
        "key": "ctrl+shift+t",
        "command": "r.test"
    }
]
```
