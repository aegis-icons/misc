# aegis-icons — Style guide

These are formatting guidelines that are used in the [CONTRIBUTING](https://github.com/aegis-icons/aegis-icons/blob/master/CONTRIBUTING.md) document.

## Useful links

- [GitHub – Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
  - [Alerts](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts), unique feature in the GitHub flavored markdown; often used in the documentation.
  - [Emojis](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#using-emojis), GitHub has own emoji system that works consistently across the different platforms compared to directly inserted emojis.

- **GitHub Emoji resources**
  - [emoji-cheat-sheet by ikatyang](https://github.com/ikatyang/emoji-cheat-sheet/blob/github-actions-auto-update/README.md), endorsed by GitHub.
  - [Emoji Cheat Sheet by WebFX](https://www.webfx.com/tools/emoji-cheat-sheet/), search engine _(set "Click to copy" to "Shortcode")_.
  - [AllGithubEmojis by jzeferino](https://jzeferino.github.io/AllGithubEmojis/), search engine _(outdated)_.
  
- ["HTML Tags You Can Use on GitHub" by seanh](https://gist.github.com/seanh/13a93686bf4c2cb16e658b3cf96807f2)

## Formatting

### General

- For _italics_, use `_ _` syntax instead of `* *`.
  - **Reason:** more recognizable then asterisks, since asterisks are used commonly with **bold text:** `** **`.

### Headings

- Use singular *hierarchy level one* heading at the top of the document, syntax: `# This is heading level 1`.

### Details block

Use it for content that's not vital, here's the format that aegis-icons uses:

```
<details>
<summary>
  <samp><ins>
    Name for the button to open and close the details
  </ins></samp>
</summary>

> The content, always insert content into "quoted text" syntax.

</details>
```
