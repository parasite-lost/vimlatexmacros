# vimlatexmacros

## Description

Vim insert mode selfexpanding LaTeX macros.

Extracted from github.com/vim-latex/vim-latex

## Mappings

Macros expand automatically and tokens (<++>) are used to mark the positions where you can fill
in your content. With a movement key you can jump to the next token so that you don't need to
worry about moving to the right position when expaanding many macros inside each other.

### Keybindings:
    C-j: go to the next token (<++>)


### Selfexpanding Macros:
Curser starts automatically at the first token.

subscript and superscript

    --  ->  _{<++>}<++>
    ^^  ->  ^{<++>}<++>

brackets

    ()  ->  (<++>)<++>
    []  ->  [<++>]<++>
    {}  ->  {<++>}<++>

mathmode brackets
    
    ((  -> \left( <++> \right) <++>
    [[  -> \left[ <++> \right] <++>
    {{  -> \left\{ <++> \right\} <++>

other math constructs:

    `/  -> \frac{<++>}{<++>}<++>
    `_  -> \bar{<++>}<++>

greek symbols: usually prefix first letter with `````

    `a  -> \alpha
    `D  -> \Delta

For additional keybindings see ftplugin/tex.vim. The syntax is easy enough to add your own
macros.
