
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Approaching Positron from RStudio

RStudio has the most complete support for R, but today many teams are
polyglot and some developers working in R learned first Python or other
languages, and prefer VS Code.

A great meeting point between users of RStudio and VS Code is Positron
because it has great built-in support for R, and is similar to both
RStudio and VS Code. But of course, there are also some differences that
may be stopping you from transitioning to Positron.

Here I show how to prepare for Positron from RStudio and how to
configure Positron to minimize the differences. I’ll help you start the
transition immediately, even if it’s not a good time to slow down.

## RStudio

### Note the similarities

Positron already includes many tools you know (and likely expect) from
RStudio:

- Tools for data science:
  - R console  
  - Panels to explore plots and data  
  - Support for Quarto  
  - Keyboard shortcuts for interactive use:
    - Send code to the R console: `ctrl+enter`  
    - Restart R: `ctrl+shift+0`  
    - Assign `<-`: `alt+-`  
    - Pipe `|>`: `ctrl+M`  
- Tools for software development:
  - Support for Shiny  
  - A panel for testing  
  - Triggering a debugger from the R console  
  - Keyboard shortcuts for building R packages with devtools:
    - `load_all()`: `ctrl+shift+L`  
    - `test()`: `ctrl+shift+T`  
    - `document()`: `ctrl+shift+D`  
    - `check()`: `ctrl+shift+E`

### Get used to the command palette

Both in RStudio and Positron you can open the command palette with
`ctrl+shift+P`. It’s by far the single most useful keyboard shortcut.
It’s worth remembering it.

Practice using it from RStudio. When you switch to Positron the command
palette will help you stay productive and gradually discover keyboard
shortcuts or other “Positron ways” to work.

### Get used to the terminal

The terminal is everywhere, including both in RStudio and Positron. Some
things you do in RStudio-specific ways can also be done from the
terminal. If you get used to that workflow from RStudio, then you can do
the same thing in the same way from Positron.

For example:

- Use `git` and `gh`: Say you’re used to working with Git and GitHub
  from RStudio’s interface. You could also learn Positron’s interface –
  which is similar – or use `git` and `gh` from the terminal in the
  exact same way.

- Use aliases: Say you’re used to running tests from the *Build* tab in
  RStudio. Instead you may set an alias and run it from the terminal.

<!-- -->

    # Pro tip: Store and reuse aliases in dotfiles (see https://dotfiles.github.io/)
    alias test="Rscript -e 'devtools::test()'"

### Install `rig`: The R Installation Manager (optional)

If you’re using RStudio, you already have R. Positron will notice and
use it automatically. However, developers coming from other languages,
particularly from Python, are used to managing language-versions more
fluidly. Take this as an opportunity to learn the best practice for
managing your R installation:

We highly recommend [rig](https://github.com/r-lib/rig) for managing R
installation. –<https://positron.posit.co/r-installations.html>

## Positron

### Installation

Download Positron [from its website
(“stable”)](https://positron.posit.co/download) or [from GitHub
(preview)](https://github.com/posit-dev/positron/releases).

The specific file and process depend on your system. Here I use the
terminal to install what suits my system, but you need to adapt it to
your own system and you can likely do it all with the mouse.

#### Stable version:

    cd /tmp && \
    wget https://cdn.posit.co/positron/prereleases/deb/x86_64/Positron-2025.02.0-171-x64.deb && \
    sudo apt-get install ./Positron-2025.02.0-171-x64.deb

#### Preview version:

    cd ~/Downloads && \
    wget https://github.com/posit-dev/positron/releases/download/2025.02.0-171/Positron-2025.02.0-171-x64.deb && \
    sudo apt-get install ./Positron-2025.02.0-171-x64.deb

### Project/folder-oriented workflow

- Positron doesn’t need an `.Rproj` file but uses other markers to
  enable an equivalent [“folder” oriented
  workflow](https://positron.posit.co/rstudio-rproj-file.html). Use
  “Open Folder”.

### Minimize the differences

Enable RStudio keybindings:

- Open Positron’s settings: `ctrl+,`.  
- Search for “Enable RStudio key mappings” and check the box.  
- You can enable RStudio
  [keybindings](https://positron.posit.co/keyboard-shortcuts.html#rstudio-keymap).

Customize keyboard shortcuts:

- “Open Keyboard Shortcuts,” search for commands, and change or set a
  shortcut.

### Learn more

- See <https://positron.posit.co/>
- Ask [copilot
  (free)](https://docs.github.com/en/copilot/managing-copilot/managing-copilot-as-an-individual-subscriber/about-github-copilot-free)
  about Positron or VS Code: <https://github.com/copilot>
