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
  - **Reason:** more recognizable on the markup then asterisks, since asterisks are used commonly with **bold text:** `** **`.
- Do not combine bold and italic together, example: `**_don't do this_**`.
  - **Reason:** read section about hierarchy level four headings.
- Do not underline the body text, <ins>like this</ins>.
  - **Reason:** too similar to links and details block's clickable object.

### Headings

- Use singular **hierarchy level one** (h1) heading at the top of the document, syntax: `# This is h1`.

- Use nested heading hierarchy, [example](https://www.w3.org/WAI/tutorials/page-structure/headings/#main-heading-before-navigation).

- Max. heading level that can be used is **four.**

- For **hierarchy level four** (h4) headings, use also italic style and add horizontal line to the top, the format:

```md

---

#### _This is h4_
```

> _Reason:_ On the Github's Markdown files, h4's font-size is unfortunately similar to bold body text, italic makes the heading more distinguish. Horizontal line makes h4 easier to scan the seperation between the body text and next h4 section.

### Line breaks

### Emojis

Use GitHub's emoji shortcodes (example: :+1: `:+1:`), because these work more consistently across the different platforms.

> _Example:_ in Android, directly inserted emojis sometimes might use one colored font or not display at all).

Resources for the emoji shortcodes, check the [useful links](#useful-links) section.

### Details block

Use it for content that's not vital, here's the format that aegis-icons uses:

```html
<details>
<summary>
  <samp><ins>
    Name for the button to open and close the details
  </ins></samp>
</summary>

> The content, always insert content into "quoted text" syntax.

</details>
```
