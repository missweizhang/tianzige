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

## Example Usage

Characters for tracing in mizige:
`\usepackage[fontsize=24, textcolor=lightgray, gridcolor=green, pycolor=blue, mizige]{tianzige}`

Characters displayed in black without grid:
`\usepackage[fontsize=24, textcolor=black, nogrid]{tianzige}`


## Options Details

Option | Values | Details 
------ | ------ | ------
fontsize | `<numeric>` | size of the Chinese character
textcolor | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | color of the Chinese character
gridcolor | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | color of the tianzige or mizige grid
pycolor | [`<colors>`](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX#Named_colours_provided_by_the_xcolor_package) | color of pinyin
nogrid | N/A | do not show tianzige or mizige, will override `gridcolor`

