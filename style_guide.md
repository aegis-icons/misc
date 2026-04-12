# aegis-icons — Style guide

These are Markdown / HTML formatting guidelines that are used in the [CONTRIBUTING](https://github.com/aegis-icons/aegis-icons/blob/master/CONTRIBUTING.md) document.
<br><br>

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
<br>

## Formatting

### General

- For _italics_, use `_ _` syntax instead of `* *`.
  - **Reason:** more recognizable on the markup then asterisks, since asterisks are commonly used with **bold text:** `** **`.
- Do not combine bold and italic together, example: `**_don't do this_**`.
  - **Reason:** read section about hierarchy level four (h4) headings.
- Do not underline the text, <ins>like this</ins>.
  - **Reason:** too similar to links and [details block](#details-block)'s clickable object.
- Only use horizontal line (`---`) for the top of the hierarchy level four (h4) headings.
<br>

### Headings

- Use singular **hierarchy level one** (h1) heading at the top of the document, syntax: `# This is h1`.

- Use nested heading hierarchy, [example](https://www.w3.org/WAI/tutorials/page-structure/headings/#main-heading-before-navigation).

- Max. heading level that can be used is **four** (h4).

- For **hierarchy level four** (h4) headings, add italic styling to heading and horizontal line above, the format:

```markdown

---

#### _This is h4_
```

> **Reason:** On the GitHub's Markdown read view, h4's font size is unfortunately similar to the bold body text. The italic makes the heading more distinguish of bold body text. Horizontal line makes it easier to scan the separation between the body text and next h4 section.
<br>

### Alerts

- Use minimal amount of alerts per section[^1].
  - **Recommended:** 1.
  - **Maximum:** 2.
  
> **Reason:** multiple alerts in a row can overwhelm and confuse the reader. We have done this mistake before and try to avoid it in the future.

The types of alerts are listed on [GitHub's documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts).
<br><br>

### Emojis

Use GitHub's emoji shortcodes (example: :+1: `:+1:`), because these work more consistently across the different platforms.

> _Example:_ on Android, directly inserted emojis sometimes might use one colored symbol instead of multicolor emojis or only display as box (a.k.a. [tofu](https://fonts.google.com/knowledge/glossary/tofu)).

Resources for the emoji shortcodes, check the [useful links](#useful-links) section.
<br><br>

### Extra line breaks

> [!IMPORTANT]
> **Don't do this if:**
> - It's the end of `h4` section, if next one is also `h4`. Do it only if next one is `h3`.
> - Between headings, for example: `h1` heading and after that, `h2` heading.

To make [CONTRIBUTING](https://github.com/aegis-icons/aegis-icons/blob/master/CONTRIBUTING.md) less dense and easier to scan, we're adding at least 2 line breaks to the end of the section[^1].

Normally GitHub Flavored Markdown only allows adding 1 line breaks to readable text after adding two line breaks to the markup, so we also need to use `<br>` HTML tag to force more line breaks.

Sometimes 3 line breaks are needed to get enough separation, because of GitHub's Markdown CSS. **Preview first before committing.**

**:bulb: Examples of extra line breaks:**

_2 line breaks:_

```markdown
THIS SECTION ENDS...
<br>

## ...NEXT SECTION STARTS
```

_3 line breaks:_

```markdown
THIS SECTION ENDS...
<br><br>

## ...NEXT SECTION STARTS
```
<br>

### Details block

Use it for content that's not vital for most of the readers, here's the format that aegis-icons uses:

```markdown
<details>
<summary>
  <samp><ins>
    This is details block's clickable object to open / close the text
  </ins></samp>
</summary>

> The content, always insert content into "quoted text" syntax.
>
> _Lorem ipsum dolor sit amet, consectetur adipiscing elit. In dolor dui, scelerisque efficitur metus quis, molestie aliquam sem. Integer quis sollicitudin nisl. Ut id tempor velit. Duis pharetra lorem at ante imperdiet semper. Sed at vulputate massa._
>
> _Sed orci tortor, accumsan at ornare sed, auctor non sapien. Integer bibendum, enim non tempus placerat, est urna varius erat, nec tincidunt dui mi eget sem. Vivamus sit amet dolor erat._

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
>
> _Lorem ipsum dolor sit amet, consectetur adipiscing elit. In dolor dui, scelerisque efficitur metus quis, molestie aliquam sem. Integer quis sollicitudin nisl. Ut id tempor velit. Duis pharetra lorem at ante imperdiet semper. Sed at vulputate massa._
>
> _Sed orci tortor, accumsan at ornare sed, auctor non sapien. Integer bibendum, enim non tempus placerat, est urna varius erat, nec tincidunt dui mi eget sem. Vivamus sit amet dolor erat._

</details>

[^1]: **Meaning of the section in this context:** it starts after the heading syntax and ends just before the next heading syntax.
