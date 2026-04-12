# aegis-icons — Style guide

These are Markdown / HTML formatting guidelines that are used in the [CONTRIBUTING](https://github.com/aegis-icons/aegis-icons/blob/master/CONTRIBUTING.md) document.

## Useful links

- [GitHub – Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
  - [Alerts](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts), unique feature in the GitHub Flavored Markdown; often used in the documentation.
  - [Emojis](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#using-emojis), GitHub has own emoji system that works consistently across the different platforms compared to directly inserted emojis.

- **GitHub Emoji resources**
  - [emoji-cheat-sheet by ikatyang](https://github.com/ikatyang/emoji-cheat-sheet/blob/github-actions-auto-update/README.md), endorsed by GitHub.
  - [Emoji Cheat Sheet by WebFX](https://www.webfx.com/tools/emoji-cheat-sheet/), search engine _(set "Click to copy" to "Shortcode")_.
  - [AllGithubEmojis by jzeferino](https://jzeferino.github.io/AllGithubEmojis/), search engine _(outdated)_.
  
- ["HTML Tags You Can Use on GitHub" by seanh](https://gist.github.com/seanh/13a93686bf4c2cb16e658b3cf96807f2)

## Formatting

### General

- For _italics_, use `_ _` syntax instead of `* *`.
  - **Reason:** more recognizable on the markup then asterisks, since asterisks are commonly used with **bold text:** `** **`.
- Do not combine bold and italic together, example: `**_don't do this_**`.
  - **Reason:** read section about hierarchy level four (h4) headings.
- Do not underline the text, <ins>like this</ins>.
  - **Reason:** too similar to links and [details block](#details-block)'s clickable object.
- Only use horizontal line (`---`) for the top of the hierarchy level four (h4) headings.

### Headings

- Use singular **hierarchy level one** (h1) heading at the top of the document, syntax: `# This is h1`.

- Use nested heading hierarchy, [example](https://www.w3.org/WAI/tutorials/page-structure/headings/#main-heading-before-navigation).

- Max. heading level that can be used is **four** (h4).

- For **hierarchy level four** (h4) headings, add italic styling to heading and horizontal line above, the format:

```md

---

#### _This is h4_
```

> _Reason:_ On the GitHub's Markdown read view, h4's font size is unfortunately similar to the bold body text. The italic makes the heading more distinguish of bold body text. Horizontal line makes it easier to scan the separation between the body text and next h4 section.

### Line breaks

### Emojis

Use GitHub's emoji shortcodes (example: :+1: `:+1:`), because these work more consistently across the different platforms.

> _Example:_ on Android, directly inserted emojis sometimes might use one colored symbol instead of multicolor emojis or only display as box (a.k.a. [tofu](https://fonts.google.com/knowledge/glossary/tofu)).

Resources for the emoji shortcodes, check the [useful links](#useful-links) section.

### Details block

Use it for content that's not vital to most of the readers, here's the format that aegis-icons uses:

```html
<details>
<summary>
  <samp><ins>
    This is details block's clickable object to open / close the text
  </ins></samp>
</summary>

> The content, always insert content into "quoted text" syntax.

</details>
```

**In action**:

<details>
<summary>
  <samp><ins>
    This is details block's clickable object to open / close the text
  </ins></samp>
</summary>

> The content, always insert content into "quoted text" syntax.

</details>
