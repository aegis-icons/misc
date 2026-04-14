# aegis-icons — Style guide

These are the Markdown / HTML formatting guidelines that are used in the [CONTRIBUTING](https://github.com/aegis-icons/aegis-icons/blob/master/CONTRIBUTING.md) document.

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

## Useful links

- [GitHub – Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).
  - [Alerts](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts), unique feature in the GitHub Flavored Markdown; often used in the documentation.
  - [Emojis](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#using-emojis), GitHub has own emoji system that works consistently across the different platforms compared to directly inserted emojis.

- **GitHub Emoji resources**
  - [emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/github-actions-auto-update/README.md) by ikatyang, endorsed by GitHub.
  - [Emoji Cheat Sheet](https://www.webfx.com/tools/emoji-cheat-sheet/) by WebFX, search engine _(set "Click to copy" to "Shortcode")_.
  - [AllGithubEmojis](https://jzeferino.github.io/AllGithubEmojis/) by jzeferino, search engine _(outdated)_.
  
- [HTML Tags You Can Use on GitHub](https://gist.github.com/seanh/13a93686bf4c2cb16e658b3cf96807f2) by seanh.
- [Basic Syntax](https://www.markdownguide.org/basic-syntax/) by Markdown Guide.

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

## Formatting

### General

- For _italics_, use `_ _` syntax instead of `* *`.
  - **Reason:** more recognizable on the markup then asterisks, since asterisks are commonly used with **bold text:** `** **`.
- Do not combine bold and italic together, example: `**_don't do this_**`.
  - **Reason:** read section about hierarchy level four (`h4`) headings.
- Do not underline the text, <ins>like this</ins>.
  - **Reason:** too similar to links and [details block](#details-block)'s clickable object.

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

### Headings

- Use singular **hierarchy level one** (`h1`) heading at the top of the document, syntax: `# This is h1`.

- Use nested heading hierarchy, [example](https://www.w3.org/WAI/tutorials/page-structure/headings/#main-heading-before-navigation).

- Max. heading level that can be used is **four** (`h4`).

- For **hierarchy level four** (`h4`) headings, add italic: `#### _This is h4_`

  > **Reason:** On the GitHub's Markdown document, `h4` has unfortunately similar font-size and weight to the bold body text. The italic makes the heading more distinguished of the bold body text.

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

### Alerts

- Use minimal amount of alerts per section[^1].
  - **Recommended:** 1.
  - **Maximum:** 2.
- Avoid putting them in a row.

  > **Reason:** More then 2 alerts and multiple alerts in a row can overwhelm the reader. We have done this mistake before and try to avoid it in the future. In cases where you want to notify with more then 2 alerts, use emojis and bold text instead.

:bulb: **If you have several notices, group them inside of single alert** if possible.

**In practice:**

> [!NOTE]
> - The first notice
> - The second notice
> - The third notice etc.

The types of alerts are listed on [GitHub's documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts).

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

### Emojis

Use GitHub's emoji shortcodes (example: :+1: is `:+1:`), because these work more consistently across the different platforms.

> **Example:** on Android, directly inserted emojis sometimes might use one colored symbols instead of multicolor emojis or only display as box (a.k.a. [tofu](https://fonts.google.com/knowledge/glossary/tofu)).

Resources for the emoji shortcodes, check the [useful links](#useful-links) section.

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

### Input actions

#### _Keyboard shortcuts_

Add keyboard key inside of `<kdb>` tag.

Square brackets means that it's macOS equivalent for the key.

Inside of the brackets, there's symbol of the key and name of the key.

---

_Syntax:_

```markdown
<kbd>Ctrl [⌘ Cmd]</kbd>+<kbd>Alt [⌥ Option]</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd>
```

**In practice:**

<kbd>Ctrl [⌘ Cmd]</kbd>+<kbd>Alt [⌥ Option]</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd>

**Snippets for keys:**

```markdown
<kbd>Ctrl [⌘ Cmd]</kbd>
```
```markdown
<kbd>Alt [⌥ Option]</kbd>
```

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

#### _Menu actions_

> [!IMPORTANT]
> Always start with "_menu:_", so that reader understands it's a menu action.

Use `<kdb>` and `<i>` tags together for menu objects.

Add this unicode arrow between menu objects: `➜` _(known as [Heavy Round-Tipped Rightwards Arrow](https://www.compart.com/en/unicode/U+279C), `U+279C`)._

---

_Syntax:_

```markdown
_menu:_ <kbd><i>name of 1st object to click</i></kbd> ➜ <kbd><i>name of 2nd object to click etc.</i></kbd>
```

**In practice:**

_menu:_ <kbd><i>name of 1st object to click</i></kbd> ➜ <kbd><i>name of 2nd object to click etc.</i></kbd>

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

### Line break for sections

> [!IMPORTANT]
> **Do not place line break between headings**, _example:_ `h1` heading and right after that, `h2` heading.

To make Markdown documents less dense and easier to scan, we're forcing a line break to the end of the section[^1] with `<br>`.

HTML comments are added front and back of the `<br>` for easier visualization when editing markup.

The markup line breaks in before and after `<br>` are important for successful section break.

---

_Syntax:_

```markdown
<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 
```

**In practice (markup):**

```markdown
## This section starts...

...this section ends...

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

## ...next section starts
```

<!-- SECTION BREAK --> <br> <!-- SECTION BREAK --> 

### Details block

Use it for content that's not vital for most of the readers.

---

_Syntax:_

```markdown
<details>
<summary>
  <samp><ins>
    This is details block's clickable object to open / close the text
  </ins></samp>
</summary>

> The content, always insert content into "blockquote" syntax.
>
> _Lorem ipsum dolor sit amet, consectetur adipiscing elit._
>
> _Sed orci tortor, accumsan at ornare sed, auctor non sapien._

</details>
```

**In practice**:

<details>
<summary>
  <samp><ins>
    This is details block's clickable object to open / close the text
  </ins></samp>
</summary>

> The content, always insert content into "blockquote" syntax.
>
> _Lorem ipsum dolor sit amet, consectetur adipiscing elit._
>
> _Sed orci tortor, accumsan at ornare sed, auctor non sapien._

</details>

[^1]: **Meaning of the section in this context:** it starts after the heading syntax and ends just before the next heading syntax.
