
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Approaching Positron from RStudio

Rstudio has the most complete support for R, but today many R developers
learned first Python or other languages, and feel more comfortable in VS
Code.

A great meeting point between RStudio and VS Code users is Positron,
because it has great support for R, and is similar to both RStudio and
VS Code. But of course there are also some differences that may be
stopping you from transitioning to Positron.

Here I show how to prepare for Positron from RStudio, and how to
configure Positron to minimize the differences. I’ll help you to start
the transition immediately, even if you can’t afford to slow down.

## RStudio

### Note the similarities

These tools exist both in RStudio and Positron. As an RStudio user you
likely expect them so we can just notice them:

- Tools for data science:
  - R console
  - Panels to explore plots and data.
  - Support for Quarto
  - Keyboard shortcuts for interactive use:
    - Send code to the R console: ctrl+enter\`
    - Restart R: `ctrl+shift+0`
    - Assign `<-`: alt+-\`
    - Pipe `|>`: `ctrl+M`
- Tools for software development:
  - Support for Shiny
  - A panel for testing
  - Triggering a debugger from the R console.
  - Keyboard shortcuts for building R packages with devtools.
    - `load_all()`: `ctrl+shift+L`
    - `test()`: `ctrl+shift+T`
    - `document()`: `ctrl+shift+D`
    - `check()`: `ctrl+shift+E`

### Get used to the commands pallete

Both in RStudio and Positron open the commands pallete with
`ctrl+shift+P`. It’s the only keyboard shortcut you must memorize.

Practice using it from RStudio. It’ll help you stay productive in
Positron before you memorize the Positron way of doing things.

### Get used to the terminal

`ctrl+shift` + “new terminal”

### Install `rig`: The R Installation Manager

> We highly recommend [rig](https://github.com/r-lib/rig) for managing R
> installation. –<https://positron.posit.co/r-installations.html>

## Positron

### Installation

Install Positron

### Minimize the differencees

You can enable RStudio
[keybindings](https://positron.posit.co/keyboard-shortcuts.html#rstudio-keymap):

- Open Positron’s settigns: `ctrl+,`.
- Search “Enable rstudio key mappings” and check the box.

## WIP

- The commands pallet: `ctrl+shift+P`
- Addins, aliases
- IDE settings
- Project-oriented workflow: `.Rproj`, `.git/`, `.here`, …
- The console/terminal,

## Positron

- Installation
- [Keyboard
  shortcuts](https://positron.posit.co/keyboard-shortcuts.html)
- [Project-oriented
  workflow](https://positron.posit.co/rstudio-rproj-file.html): Open
  Folder \> In Positron, the words folder, “workspace”, and “project”
  are used almost interchangeably,
- `.vscode/settings.json`
