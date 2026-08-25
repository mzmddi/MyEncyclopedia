# Markdown Cheatsheet

## Text Formatting

_Italic text_ using single asterisks or _underscores_.  
**Bold text** using double asterisks or **underscores**.  
**_Bold and italic_** using triple asterisks.  
~~Strikethrough~~ text using double tildes.  
Subscript: H<sub>2</sub>O  
Superscript: x<sup>2</sup>

---

## Headings

```
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
```

---

## Lists

### Unordered Lists

- Item 1
- Item 2
  - Sub-item 2.1
  - Sub-item 2.2

* Alternative hyphen bullet

### Ordered Lists

1. First step
2. Second step
   1. Sub-step 2.1
   2. Sub-step 2.2
      1. Sub-Sub-step 2.2.1
      2. Sub-Sub-step 2.2.2
         1. Sub-Sub-Sub-step 2.2.2.1
3. Third step

### Task Lists / Checklists

- [x] Completed task
- [ ] Incomplete task
- [ ] Future task

---

## Links & Images

```
[Link Text](https://example.com "Optional Hover Title")
```

```
[Relative Link](./other-file.md)
```

```
![Image Alt Text](path/to/image.png "Optional Image Title")
```

### File & Code Linking Across Repositories

You can link relative files in your directory tree, reference explicit commit hashes, or link line numbers directly.

```
[Python Notes](../Languages/python/syntax.md) (Relative file path)
```

```
Relative image display: `![Architecture Diagram](./assets/arch.png)`
```

- Intra-Repo (Relative Path): Links within your knowledge-base repository use relative paths.  
  `[Python Syntax](../Languages/python/syntax.md)`

- Inter-Repo (Absolute URL): To link from your encyclopedia repo to a file in a different repository. You must use the absolute URL. `
[View Project Source Code](https://github.com/your-username/my-project/blob/main/src/main.cpp)`

### Linking Across Repositories - Specific Lines or Line Ranges

When linking to specific code in another repository, click the line number on GitHub to generate a direct link. Append `#L` and line numbers to the file URL.

Linking to line 42:

```
[Main Loop Setup](https://github.com/user/repo/blob/main/src/app.py#L42)
```

Linking to line range 15-30:

```
[Configuration Block](https://github.com/user/repo/blob/main/src/app.py#L15-L30)
```

### Permalinks

If you link to blob/main/src/app.py#L42, that link might point to the wrong code later if you edit or add lines to app.py.

To create a permalink that stays frozen on the exact code state:

1. Open the file on Github.
2. Press the key `y` on your keyboard.
3. Github replaces `main` in the URL (top of the browser, in the URL line) with the exact commit hash.
4. Use that specific URL with the commit hash.

```
[Ray-Object Intersection Routine](https://github.com/user/repo/blob/a1b2c3d4e5f6/src/raytracer.cpp#L102-L120)
```

## Blockquotes

> Single-line blockquote.
>
> Multi-paragraph blockquote.
>
> > Nested blockquote.

---

## Code & Syntax Highlighting

Inline `code` using single backticks.

```python
# Fenced code block with syntax highlighting
def greet(name: str) -> str:
    return f"Hello, {name}!"
```

## Tables

Use pipes `|` to separate columns, and hyphens `-` for the header row.
Colons `:` control text alignment within columns.

| Left Aligned | Centered | Right Aligned |
| :----------- | :------: | ------------: |
| Python       |   3.12   |          Fast |
| C++          |    20    |        Faster |
| Markdown     |   GFM    |    Plain Text |

### Table Column Alignment Types

| Left Aligned (`:---`) |  Centered (`:---:`)  | Right Aligned (`---:`) | Default (`---`)  |
| :-------------------- | :------------------: | ---------------------: | ---------------- |
| Colon on the left     | Colons on both sides |     Colon on the right | No colons        |
| Align text/labels     | Align status/badges  |   Align numbers/prices | Defaults to left |

---

### Number of Hyphens

**Number of Hyphens:** You only need a minimum of 3 hyphens (`---`), but you can add more if you want to align your raw text visually in your text editor:

```markdown
| Short | Long Header Title |
| :---- | :---------------- |
| Item  | Description       |
```

---

### Line Breaks (ENTER) inside a Table

Line Breaks inside Cells: Markdown does not allow pressing Enter inside a table cell. Use HTML <br> tags to force a new line:

| Concept  | Details                   |
| :------- | :------------------------ |
| Markdown | Fast<br>Clean<br>Portable |

---

### Using Pipeline `|` inside a Table

Escaping Pipes: If you need to use a pipe symbol `|` inside a table cell's text, escape it with a backslash `\|`

| Operator | Meaning                    |
| :------: | :------------------------- |
|  `\|\|`  | Logical OR in C++ / Python |

---

### Inline Formatting, Inline Code, Links, Bold/Italics inside a Table

You can use inline formatting, inline code backticks, links, and bold/italics inside table cells.

| Concept         |    Syntax     | Example                                |
| :-------------- | :-----------: | :------------------------------------- |
| **Inline Code** | `` `code` ``  | Use `std::cout` in C++                 |
| **Emphasis**    |  `**bold**`   | **Crucial step**                       |
| **Links**       | `[Text](URL)` | [GitHub Docs](https://docs.github.com) |

---

### Merging Cells (HTML Fallback)

Markdown natively **does not support** merging rows (`rowspan`) or columns (`colspan`). If you need merged cells, use raw HTML inside your `.md` file.

<table>
  <tr>
    <th>Category</th>
    <th>Format</th>
    <th>Extension</th>
  </tr>
  <tr>
    <td rowspan="2">Documents</td>
    <td>Markdown</td>
    <td><code>.md</code></td>
  </tr>
  <tr>
    <td>LaTeX</td>
    <td><code>.tex</code></td>
  </tr>
</table>

## Task Lists (Checkboxes)

Interactive checkboxes supported by GitHub and local editors like Obsidian.

- [x] Set up repository structure
- [x] Create `Formats and Protocols/` directory
- [ ] Add advanced Markdown notes

---

## Collapsible Sections (HTML Details)

Hide long code blocks, logs, or detailed notes behind a togglable dropdown.  
The collapsible sections can be nested within themselves, by having valid and correct `<details></details>` wrappings.

<details>
<summary>Click to expand</summary>

```text
Lorem Ipsum
```

</details>

<details>
<summary>Click to expand this one</summary>

<details>

<summary>This is a nested collapsible section. FIRST</summary>

```text
This is the FIRST nested text section
```

</details>

<details>

<summary>This is a nested collapsible section. SECOND</summary>

```text
This is the SECOND nested text section
```

</details>

</details>

## Heading Anchors

GitHub automatically generates an anchor ID for every heading in your document, allowing you to link directly to any section using standard `[Link Text](#heading-anchor)` syntax.

### 3 Rules for Heading Anchors

1. Lowercase everything: Convert the heading text to all lowercase letters.
2. Replace spaces with hyphens: Change spaces between words into single hyphens (-).
3. Remove special characters: Strip out punctuation, code backticks, parentheses, colons, and symbols.

### Examples of Using Header Anchors

```
## Table Column Alignment Options
 ||
 \/
#table-column-alignment-options
```

```
### C++ & Python (2026)
 ||
 \/
#c--python-2026
```

```
### Table of Contents Example
- [Text Formatting](#text-formatting)
- [Lists](#lists)
- [Code & Syntax Highlighting](#code--syntax-highlighting)
- [Advanced Table Tricks](#advanced-table-tricks--edge-cases)
```

| Original Heading Text                    | Generated Anchor ID                  | Markdown Link Syntax                         |
| :--------------------------------------- | :----------------------------------- | :------------------------------------------- |
| `## Text Formatting`                     | `#text-formatting`                   | `[Jump](#text-formatting)`                   |
| `### Advanced Table Tricks & Edge Cases` | `#advanced-table-tricks--edge-cases` | `[Jump](#advanced-table-tricks--edge-cases)` |
| `### Step 1: Install Node.js`            | `#step-1-install-nodejs`             | `[Jump](#step-1-install-nodejs)`             |
| `## Return to Top`                       | `#` (Top of document)                | `[Top](#)`                                   |

### Using HTML Anchors if Markdown doesnt work

If a heading has complex characters or you want a fixed link that doesn't change when you rename the heading:

<a name="custom-target"></a>

### My Long Heading Title

Link to it anytime using: `[Jump to Section](#custom-target)`
