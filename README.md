# Markdown Extension Pack

This extension pack packages some of the most popular (and some of my favorite) Markdown extensions. If you like it, please leave your `Rating & Review` and share with your friends. If you know any extension that is good for Markdown authoring, just let me know by [creating an issue](https://github.com/doggy8088/markdown-extension-pack/issues).

## Extensions Included

### Linting Tool

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

  Markdown linting and style checking for Visual Studio Code. Check [Rules](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md) for more details.

  When you get rule violations (wavy underlined text) in a doc, it support **Quick Fix**.

  Useful Shortcuts:

  - Windows
    - `Ctrl + .` : Quick Fix
  - macOS
    - `⌘ + .` : Quick Fix

  > I use [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) to validate my Markdown files. But some of the rules might break your content by accident if you enabled **Editor: Format On Save** (`editor.formatOnSave`) setting. Below is my `.markdownlint.json` file which disabled some rules that I don't need. Especially the [MD044 - Proper names should have the correct capitalization](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md#md044---proper-names-should-have-the-correct-capitalization) might broken some of the **Terms** in your doc.

  ```json
  {
    "MD001": false,
    "MD012": false,
    "MD013": false,
    "MD028": false,
    "MD034": false,
    "MD041": false,
    "MD044": false,
    "MD029": {
      "style": "ordered"
    }
  }
  ```

### Editing Tools

- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)

  Useful Shortcuts:

  - Windows
    - `Ctrl + B` : Toggle bold
    - `Ctrl + I` : Toggle italic
    - `Alt + S` : Toggle strikethrough
    - `Alt + C` : Check/Uncheck task list item
    - `Ctrl + Shift + ]` : Toggle heading (uplevel)
    - `Ctrl + Shift + [` : Toggle heading (downlevel)
    - `Alt + Shift + F` : Format Document with a Table formatter
  - macOS
    - `Alt + C` : Check/Uncheck task list item
    - `Cmd + B` : Toggle bold
    - `Cmd + I` : Toggle italic
    - `Cmd + Shift + ]` : Toggle heading (uplevel)
    - `Cmd + Shift + [` : Toggle heading (downlevel)
    - `Alt + Shift + F` : Format Document with a Table formatter

- [Markdown Paste](https://marketplace.visualstudio.com/items?itemName=telesoho.vscode-markdown-paste-image)

  Useful Shortcuts:

  - `Ctrl + Alt + V` : Simply copy a image to Clipboard then use `Ctrl+Alt+V` to paste into your doc.

    > You can paste not only images, but also any Text, HTML, Rich-Text to Markdown.

- [Excel to Markdown table](https://marketplace.visualstudio.com/items?itemName=csholmq.excel-to-markdown-table)

  Useful Shortcuts:

  - `Shift + Alt + V` : Copy a region of Excel Spreadsheet then use `Shift+Alt+V` to paste into a markdown doc in a table from.

- [CSV to Markdown Table Converter](https://marketplace.visualstudio.com/items?itemName=Marchiore.csvtomarkdown)

   Paste CSV to Markdown doc. Select the corresponding text to CSV. Hit `F1` and select **Convert CSV to Markdown Table** command. Done!

### Markdown Preview enhancements

- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)

  Changes VS Code's built-in markdown preview to match GitHub's styling.

- [Markdown Image Size](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-image-size)

  Adds `![](IMAGEURL =100x200)` image size syntax support to VS Code's built-in Markdown preview.

  > Azure DevOps's Wiki page support [resize image](https://docs.microsoft.com/en-us/azure/devops/project/wiki/markdown-guidance?view=azure-devops&WT.mc_id=DT-MVP-4015686#images) syntax.

- [Markdown Preview Mermaid Support](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)

  Adds [Mermaid](https://mermaid-js.github.io/mermaid/) diagram and flowchart support to VS Code's builtin markdown preview

  It support both `::: mermaid` and ` ```mermaid ` syntax.

  > Azure DevOps's Wiki page [support Mermaid diagram](https://docs.microsoft.com/en-us/azure/devops/project/wiki/wiki-markdown-guidance?view=azure-devops&WT.mc_id=DT-MVP-4015686#add-mermaid-diagrams-to-a-wiki-page) syntax.

- [Markdown Emoji](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-emoji)

  Adds [:emoji:](https://www.webpagefx.com/tools/emoji-cheat-sheet/) syntax support to VS Code's built-in Markdown preview.

- [Markdown yaml Preamble](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-yaml-preamble)

  Renders YAML front matter as a table in the built-in markdown preview.

- [Markdown Footnotes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-footnotes)

  Adds `[^1]` footnote syntax support to VS Code's built-in Markdown preview

### Misc. Utilities

- [Copy Markdown as HTML](https://marketplace.visualstudio.com/items?itemName=jerriepelser.copy-markdown-as-html)

  I'll turn markdown into HTML and put it onto Clipboard. No file will be generated. It is very useful that when I writing posts.

- [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

  You can right-click on any folder in the **EXPLORER** pane and choose **Generate .editorconfig** command.

  ```ini
  root = true

  [*]
  indent_style = space
  indent_size = 4
  end_of_line = crlf
  charset = utf-8
  trim_trailing_whitespace = true
  insert_final_newline = false

  [*.md]
  indent_size = 2
  ```

### Customizable Shortcuts

1. **Insert Snippet** (`editor.action.insertSnippet`)

   `Ctrl + K` : Insert Link on selected text

   > Your can just paste link from clipboard on selected text if you installed [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) extension which is already included in this extension pack.

2. **Snippets for Markdown** (`editor.action.triggerSuggest`)

   `Ctrl + Space` : Trigger suggest

3. **Markdown: Open Preview** (`markdown.showPreview`)

   I'll remove the built-in `Ctrl + Shift + V` for this command. There is another shortcut registered below:

   `Ctrl + Shift + Alt + P` : Open Preview

4. **Markdown: Open Preview to the side** (`markdown.extension.togglePreview`)

   The default `Ctrl + K V` will not available if your installed [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one). So you have to customize the built-in Keyboard Shortcuts to `Ctrl + Shift + V`.

   `Ctrl + Shift + V` : Open Preview to the side (The 2nd editor)

   > You can hit the same hotkey to close the Preview.

### Extensions NOT Included but might be useful

You need to install the following extensions manually if you need:

- [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)

  Markdown Preview Enhanced is an extension that provides you with many useful functionalities such as automatic scroll sync, [math typesetting](https://shd101wyy.github.io/markdown-preview-enhanced/#/math), [mermaid](https://shd101wyy.github.io/markdown-preview-enhanced/#/diagrams?id=mermaid), [PlantUML](https://shd101wyy.github.io/markdown-preview-enhanced/#/diagrams?id=plantuml), [pandoc](https://shd101wyy.github.io/markdown-preview-enhanced/#/pandoc), PDF export, [code chunk](https://shd101wyy.github.io/markdown-preview-enhanced/#/code-chunk), [presentation writer](https://rawgit.com/shd101wyy/markdown-preview-enhanced/master/docs/presentation-intro.html), etc. A lot of its ideas are inspired by [Markdown Preview Plus](https://github.com/atom-community/markdown-preview-plus) and [RStudio Markdown](http://rmarkdown.rstudio.com/).

- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

  There is a **Format Document (Forced)** command (`prettier.forceFormatDocument`) that can format your Markdown document by force!

  I'll bind `Ctrl + Alt + Shift + F` hotkey to this command.

- [Markdown+Math](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath)

  If you want to use this extension, please remember disable `math.enabled` option.

- [Medium to Markdown](https://marketplace.visualstudio.com/items?itemName=moshfeu.vscode-medium-to-markdown)

  Import your Medium posts into Markdown in your editor.

### Code Snippets

| Prefix    | Description                         |
| --------- | ----------------------------------- |
| ` ``` `   | fenced code blocks                  |
| `details` | Use `<details>` element in Markdown |

### Useful links

- [Markdown and Visual Studio Code](https://code.visualstudio.com/Docs/languages/markdown)

**Enjoy!**
