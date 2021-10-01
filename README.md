# Installation on MiKTeX in Windows

## [Create a local TEXMF root directory](https://miktex.org/faq/local-additions)
1. Create a local directory to store your latex package files, such as `C:\localtexmf\tex\latex\`, 

2. Copy your `tianzige.sty` file into the local directory as
`C:\localtexmf\tex\latex\tianzige\tianzige.sty`

![image](https://user-images.githubusercontent.com/19189069/135584016-5caba78c-517d-455b-85d5-eb5addbf3b79.png)

## [Register the local directory as the TEXMF root directory](https://miktex.org/howto/miktex-console)

3. Start `MiKTeX Console`

4. Click `Settings`

5. Click the `Directories` tab.  

6. Click the `Add` toolbar button,

7. Select the TEXMF root directory `C:\localtexmf\tex\latex\` to add.

Now you are ready to use the `tianzige` package in your latex code.

# Using the `tianzige` package in latex code

## Overview

Including the `tianzige` package in your latex document allows you to use the `\grid` and `\pygrid` commands which draws a grid to enclose a Chinese character given as argument to he command.  You may specify options upon including the package to specify the style of the grid and the font size and color of the character enclosed.

Note: The `.tex` document that includes the `tianzige` package must be compiled using `XeLaTeX`.

## Usage: `tianzige` package options

Characters for tracing in mizige:
`\usepackage[fontsize=24, textcolor=lightgray, gridcolor=green, pycolor=blue, mizige]{tianzige}`

Characters displayed in tianzige:
`\usepackage[fontsize=24, textcolor=black, gridcolor=red, pycolor=brown]{tianzige}`

Characters displayed in black without grid:
`\usepackage[fontsize=24, textcolor=black, nogrid]{tianzige}`

## `tianzige` package options details

Options can be written in any order.

### `tianzige` package regular options
Option | Default | Details 
------ | ------- | ------
`mizige` | off | show mizige instead of tianzige
`nogrid` | off | do not show tianzige or mizige, will override `gridcolor`

### `tianzige` package options as key/value pairs

Option | Values | Default | Details 
------ | ------ | ------- | ------
`fontsize` | `<numeric>` | `24` | size of the Chinese character
`textcolor` | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | `lightgray` |color of the Chinese character
`gridcolor` | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | `red` | color of the tianzige or mizige grid
`pycolor` | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | `black` | color of pinyin

## Usage: `\grid` and `\pygrid` commands
The document that includes the `tianzige` package is free to call the following commands to draw tianzige or mizige.

`\grid{}` draws an empty grid

`\grid{天}` draws a grid enclosing the character 天

`\pygrid{天}{tian1}` draws a grid enclosing the character 天 and includes its pinyin above the character

`\pygrid{}{tian1}` draws an empty grid with pinyin above the grid

## Use `\grid` and `\pygrid` commands with options

The commands `\grid` and `\pygrid` share most options except `pycolor`.  Options are accepted as the first argument in `[]` brackets as key-value pairs.

`\pygrid[fontsize=52]{天}{tian1}` draws a grid enclosing a size-52 character 天

`\grid[grid=false, color=red]{红}` draws the character 红 in red without a grid

`\pygrid[pycolor=red, color=lightgray]{}{hong2}` draws a red grid enclosing the character 红 in lightgray

### `\grid` and `\pygrid` command option details

Options can be written in any order.

Option | Values | Default | Details 
------ | ------ | ------- | ------
`fontsize` | `<numeric>` | `24` | size of the Chinese character
`color` | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | `lightgray` |color of the Chinese character
`pycolor` | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | `black` | color of pinyin
`grid` | `true` or `false` | `true` | color of the tianzige or mizige grid


