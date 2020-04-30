---
title: Grammar, formatting, and style
description: Learn the syntax and formatting rules for writing documentation for the Filecoin project.
---

# Grammar, formatting, and style

This page details the syntax and formatting rules for writing Filecoin documentation. For more conceptual ideas of writing, check out the [writing guide](/community/contribute/writing-guide/).

## Grammar and spelling

Here are some language-specific rules that the Filecoin documentation follows. If you use a writing service like [Grammarly](https://www.grammarly.com/), most of these rules are turned on by default.

### American English

While Filecoin is a global project, the fact is that American English is the most commonly used _style_ of English used today. With that in mind, when writing content for the Filecoin project, use American English spelling. The basic rules for converting other styles of English into American English are:

1. Swap the `s` for a `z` in words like _categorize_ and _pluralize_.
2. Remove the `u` from words like _color_ and _honor_.
3. Swap `tre` for `ter` in words like _center_.

### The Oxford comma

Follow each list of three or more items with a comma `,`:

| Use                           | Don't use                    |
| ----------------------------- | ---------------------------- |
| One, two, three, and four.    | One, two, three and four.    |
| Henry, Elizabeth, and George. | Henry, Elizabeth and George. |

### Acronyms

If you have to use an acronym, spell the full phrase first and include the acronym in parentheses `()` the first time it is used in each document. Exception: This generally isn't necessary for commonly-encountered acronyms like _IPFS_, unless writing for a stand-alone article that may not be presented alongside project documentation.

> Virtual Machine (VM), Decentralized Web (DWeb).

## Formatting

How the Markdown syntax looks, and code formatting rules to follow.

### Syntax

The Filecoin Docs project follows the _GitHub Flavoured Markdown_ syntax for markdown. This way, all articles display properly within GitHub itself. This gives readers the option to view articles on [the docs website](https://filecoin-docs.netlify.app) or [its GitHub repo](https://github.com/filecoin-project/filecoin-docs).

### Rules

We use the rules set out in the [VSCode Markdownlint](https://github.com/DavidAnson/vscode-markdownlint) extension. You can import these rules into any text editor like Vim or Sublime. All rules are listed [within the Markdownlint repository](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md).

We highly recommend installing [VSCode](https://code.visualstudio.com/) with the [Markdownlint](https://github.com/DavidAnson/vscode-markdownlint) extension to help with your writing. The extension shows warnings within your markdown whenever your copy doesn't conform to a rule.

![Screenshot of some Markdown in VSCode showing an error.](./images/grammar-formatting-and-style/no-empty-links-error.png)

The extension summarizes all the warnings within the open file at the bottom of the editor:

![Screenshot of VSCode with a summary of markdown errors.](./images/grammar-formatting-and-style/markdown-error-summary.png)

## Style

The following rules explain how we organize and structure our writing. The rules outlined here are in addition to the [rules](https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md) found within the [Markdownlinter extension](https://github.com/DavidAnson/vscode-markdownlint).

### Text

The following rules apply to editing and styling text.

#### Titles

1. All titles follow sentence structure. Only _names_ and _places_ are capitalized, along with the first letter of the title. All other letters are lower-case:

   ```markdown
   ## This is a title

   ### Only capitalize names and places

   #### The capital city of France is Paris
   ```

2. Every article starts with a _front-matter_ title and description:

   ```markdown
   ---
   title: Example article
   description: This is a brief description that shows up in link teasers in services like Twitter and Slack.
   ---

   ## This is a subtitle

   Example body text.
   ```

   In the above example `title:` serves as a `<h1>` or `#` tag. There is only ever one title of this level in each article.

3. Titles do not contain punctuation. If you have a question within your title, rephrase it as a statement:

   ```markdown
   <!-- This title is wrong. -->

   ## What is Filecoin?

   <!-- This title is better. -->

   ## Filecoin explained
   ```

#### Bold text

Double asterisks `**` are used to define **boldface** text. Use bold text when the reader must interact with something displayed as text: buttons, hyperlinks, images with text in them, window names, and icons.

```markdown
In the **Login** window, enter your email into the **Username** field and click **Sign in**.
```

#### Italics

Underscores `_` are used to define _italic_ text. Style the names of things in italics, except input fields or buttons:

```markdown
Here are some American things:

- The _Spirit of St Louis_.
- The _White House_.
- The United States _Declaration of Independence_.

Try entering them into the **American** field and clicking **Accept**.
```

Quotes or sections of quoted text are styled in italics and surrounded by double quotes `"`:

```markdown
In the wise words of Winnie the Pooh _"People say nothing is impossible, but I do nothing every day."_
```

#### Code blocks

Tag code blocks with the syntax of the core they are presenting:

````markdown
    ```javascript
    console.log(error);
    ```
````

##### Command-line examples

Write command-line inputs without any other characters. Precede outputs from the command line with a greater-than sign `>`. Include an empty line between the input and output of a command-line example:

````markdown
    ```bash
    lotus-storage-miner info

    > ~/lotus> lotus-storage-miner info
    > Miner: t0103
    > Sector Size: 16.0 MiB
    > Power: 0 B / 16.0 MiB (0%)
    > Worker use:
            Local: 0 / 2 (+1 reserved)
            **Remote: 0 / 1**
    > PoSt Submissions: Not Proving
    > Sectors:  map[Committing:0 Proving:0 Total:0]
    ```
````

Command-line examples can be truncated with three periods `...` to remove extraneous information:

````markdown
    ```bash
    lotus-storage-miner info

    > ~/lotus> lotus-storage-miner info
    > Miner: t0103
    > Sector Size: 16.0 MiB
    > ...
    > Sectors:  map[Committing:0 Proving:0 Total:0]
    ```
````

#### Inline code tags

Surround directories, file names, and version numbers between inline code tags `` ` ``.

```markdown
Version `1.2.0` of the program is stored in `~/code/examples`. Open `exporter.exe` to run the program.
```

#### List items

All list items follow sentence structure. Only _names_ and _places_ are capitalized, along with the first letter of the list item. All other letters are lowercase:

1. Never leave Nottingham without a sandwich.
2. Brian May played guitar for Queen.
3. Oranges.

List items end with a period `.`, or a colon `:` if the list item has a sub-list:

1. Charles Dickens novels:
   1. Oliver Twist.
   2. Nicholas Nickelby.
   3. David Copperfield.
2. J.R.R Tolkien non-fiction books:
   1. The Hobbit.
   2. Silmarillion.
   3. Letters from Father Christmas.

##### Unordered lists

Use the dash character `-` for un-numbered list items:

```markdown
- An apple.
- Three oranges.
- As many lemons as you can carry.
- Half a lime.
```

#### Special characters

Whenever possible, spell out the name of the special character, followed by an example of the character itself within a code block.

```markdown
Use the dollar sign `$` to enter debug-mode.
```

#### Keyboard shortcuts

When instructing the reader to use a keyboard shortcut, surround individual keys in code tags:

```bash
Press `ctrl` + `c` to copy the highlighted text.
```

The plus symbol `+` stays outside of the code tags.

### Images

The following rules and guidelines define how to use and store images.

#### Alt text

All images contain alt text so that screen-reading programs can describe the image to users with limited sight:

```markdown
![Screenshot of an image being uploaded through the Filecoin command line.](images/filecoin-image-upload-screen.png)
```

#### Storage location

Store images in a folder called `images` within the same directory as the article the image is presented in. If there are several articles within the same directory, create a new folder within `images` for each article. For example the article `proof-of-spacetime.md` contains the following line:

```markdown
![Proof of Spacetime diagram.](images/proof-of-spacetime/post-diagram.png)
```

The directory structure of this article looks like this:

```text
concepts/
├── content-addressed-data.md
├── images
│   └── proof-of-spacetime
│       └── post-diagram.png
└── proof-of-replication.md
└── proof-of-spacetime.md
```

There are no images within the `proof-of-replication.md` article, so there is no folder within the `images` directory for that article.

### File names

All file names are lower-case with dashes `-` between words, including image files:

```text
concepts/
├── content-addressed-data.md
├── images
│   └── proof-of-spacetime
│       └── post-diagram.png
└── proof-of-replication.md
└── proof-of-spacetime.md
```