# Atom Markdown Auto-Preview

## Blurb

Automatically activates the preview tab corresponding to a Markdown source file (if open in a different pane).
Works a treat with `markdown-scroll-sync`!

![Screencap in action](https://cloud.githubusercontent.com/assets/10861177/20911665/ad3c5d84-bbbd-11e6-97c5-6a0270c310ef.gif)

## Features

* When switching to a Markdown file, makes the first corresponding preview active (visible)
  * If it has already been opened
  * Is in a different pane/group to the source file

* When closing a Markdown file, closes any corresponding previews

## Fiddly bits

The module works on the following logic:
  * If the previewer exists, and
  * If the previewer is in a different pane, then
  * Make the previewer visible

The module scans all open tabs for ones which have an 'editor' property, to identify preview-type tabs

The 'editor' property must match the editor which has just been made active:
  * Sometimes this fails after reloading a window or in similar circumstances
  * The preview tabs persist, but this link back to the source editor is no longer valid (a limitation of Atom)
