![TagSurfer Banner](https://raw.githubusercontent.com/jrddp/tagsurfer/main/images/Banner.png)

<h2 align="center">Streamline tag creation and navigation in HTML, JSX, and more.</h2>

## Commands

### Surround with Tag

Surrounds the selected text with a new tag.

- When surrounding an inline selection, the tag defaults to a `<span>` and surrounds selected text directly.
- When surrounding a block selection, the tag defaults to a `<div>` and surrounds selected text on surrounding lines.
  - These are both configurable via `tagSurfer.defaultBlockTag` and `tagSurfer.defaultInlineTag`.

The cursor will be placed at the start of the name of the new opening tag, so it can be easily edited. I recommend using this alongside the Auto Rename Tag extension.

### Jump to Matching Pair

This combines the functionality of the Go to Matching Pair command from Emmet or Vim's '%' command.

- When the cursor is on some kind of bracket, it will jump to the matching bracket.
- When the cursor is inside a tag, it will jump to the matching closing tag.

_Additional notes:_

- If there is no bracket or tag under the cursor, it will use the bracket at the end of the line. This allows, for example, jumping to the end of a function while hovering over its name.
- If you have a full line selected, it will also jump as if you were hovering over the end of the line. This allows you to very easily select entire functions.

## Configuration

- `tagSurfer.defaultInlineTag`: Default tag for surrounding inline selections (string, default: "span")
- `tagSurfer.defaultBlockTag`: Default tag for surrounding block selections (string, default: "div")
- `tagSurfer.defaultSelfClosingTag`: Default tag for inserting self-closing tags (string, default: "div")
- `tagSurfer.autoRename`: If true, will automatically open rename prompt after creating tags. (boolean, default: false)
  - I prefer to leave this off and change the tag type manually so that I can have intellisense.

## Don't other extensions already do these things?

There are plenty of extensions that provide tag surrounding functionality, such as Surround with Tag, htmltagwrap, or Wrap It. I made this extension to avoid the following:

- Awkward formatting when creating tags
- Incompatibility with VSCode's Vim extension
- Clunky workflow when creating empty JSX tags

TagSurfer solves all of these problems.

Similarly, I created the Jump to Matching Pair feature to avoid having seperate keybinds for Vim's '%' command and Emmet's 'Go to Matching Pair' command.
