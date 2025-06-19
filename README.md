## Table of Content

1. [[#Markup vs Markdown - What’s the Difference?]]
	- [MarkUp](#markup)
	- [MarkDown](#markdown)
	- [Difference](#difference)
2. [[#Basic Content]]
	- [Headings](#headings)
	- [Text Emphasis](#text-emphasis)
	- [Horizontal Rules](#horizontal-rules)
	- [Lists](#lists)
	- [CheckLists](#checklists)
	- [Links](#links)
	- [Images](#images)
	- [References](#references)
	- [Tables](#tables)
	- [BlockQuotes](#blockquotes)
	- [Code Blocks](#code-blocks)
	- [Comments](#comments)
3. [[#Markdown Characters CheatSheet]]
4. [[#Obsidian Wiki-Links]]
## Markup vs Markdown - What’s the Difference?

### MarkUp

A Markup language is not a programming language.  It is used to define a **structure** for data and add **semantic meaning** to everything. Some famous markup languages are ***HTML, SGML*** and ***XML***. These Languages are complex and not easily readable. It is used for creating designs, web pages and scientific reports etc.

### MarkDown

A Markdown language is a lightweight version of **Markup Language**. Unlike markup language it is **human friendly** and is usually used for creating notes, blog posts and articles etc. You might find a ***README.md*** file in several places, that file is written in Markdown language to maintain documentation or description about the specific Item.

[Back to Top](#table-of-content)

---

### Difference

| Aspect      | MarkUp                                             | MarkDown                            |
| ----------- | -------------------------------------------------- | ----------------------------------- |
| General use | Creating Structures, Giving Semantic Meaning       | Simplifying content with Plain Text |
| Complexity  | More Complex, But Flexible                         | Simple and Easy, but Inflexible     |
| Usage       | Creating designs, web pages and scientific reports | Creating Notes, Blog Posts          |

[Back to Top](#table-of-content)

---
## Basic Content

### Headings

Use different no of  ***#*** to represent respective level of Heading
```markdown
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
[Back to Top](#table-of-content)

---

### Text Emphasis

Use `*` or `_` to emphasize text. Single ( `*` or `_` ) for *Italic* or double ( `**` or `__` ) for **bold**. But it is recommended to use `*` rather then `_`.

- Bold 
	1. **Bold**: ( `**Bold**` )
	2. __Bold__: ( `__Bold__` )

- Italic
	1. *Italic*: ( `*Italic*` )
	2. _Italic_: ( `Italic` )

- Bold Italic
	1. ***Bold Italic***: ( `***Bold Italic***` )
	2. ___Bold Italic___: ( `___Bold Italic___` )
	3. **Bold *Italic***: ( `**Bold *Italic***` )
	4. __Bold _Italic___: ( `__Bold _Italic___` )

[Back to Top](#table-of-content)

---

### Horizontal Rules

To add a horizontal rule use `***` , `---` or `___`. Make sure there is an empty line above and below it to avoid format defects.  Any of the above will result in

[Back to Top](#table-of-content)

---

### Lists
You can create ordered or unordered lists using `*` ,`-` or `1. ` respectively. Use Enter and Tab to create a SubList. 

#### UnOrdered List

* Bullet 1
* Bullet 2
- Bullet 1
- Bullet 2
```markdown
* Bullet 1
* Bullet 2
- Bullet 1
- Bullet 2
```

#### Ordered List
1. Numbering 1
2. Numbering 2
3. Numbering 3
4. Numbering 4

```markdown
1. Numbering 1
2. Numbering 2
3. Numbering 3
4. Numbering 4
```

> For Ordered List make sure the first number starts from 1, the rest of count doesn't matter.

[Back to Top](#table-of-content)

---

### CheckLists
To create a CheckLists use list bullet and Brackets `- [ ]` and use `x` instead of empty space to mark it as checked (done).

- [ ] Task 1
* [ ] Task 2
1. [ ] Task 3
- [x] Task 4

```markdown
- [ ] Task 1
* [ ] Task 2
1. [ ] Task 3
- [x] Task 4
```

[Back to Top](#table-of-content)

---

### Links
To use links type the name of text for link in brackets `[Text]` immediately followed by `(url)`. For Example

>`[Google](https://www.google.com/)` 

##### Output: 
 [Google](https://www.google.com/).

You can also Navigate to specific heading of the page using `#name` instead of url and replacing  spaces with `-`. Like going to
> `[Table of Contents](#table-of-content)` 

##### Output: 
[Table of Contents](#table-of-content)

Make sure not to use symbols in heading names.

[Back to Top](#table-of-content)

---

### URLs and Email Addresses

To quickly turn a URL or email address into a link, enclose it in angle brackets.

```markdown
<https://www.markdownguide.org>
<fake@example.com>
```

##### Output:
[https://www.markdownguide.org](https://www.markdownguide.org/)  
[fake@example.com](mailto:fake@example.com)

[Back to Top](#table-of-content)

---

### Images
To use Images type `!` then the Image alt text for link in brackets `[Text]` immediately followed by `(url)`.  The only difference between links and images is `!` in the beginning of image.

>`![Google](https://cdn1.iconfinder.com/data/icons/google-s-logo/150/Google_Icons-09-1024.png)` will show 

![Google](https://cdn1.iconfinder.com/data/icons/google-s-logo/150/Google_Icons-09-1024.png)

[Back to Top](#table-of-content)

---

### References
You can use reference to define a link or url once and reuse it again and again. To define it use 
`[ref name]: link`  or `[ref name]: <link>` 
and use it like `[Text][ref name]`. Make sure there is empty line above and below the ref you are creating, otherwise reference might not work properly.  

If you want to add a label when someone hover overs the text, you can add label using (quotes or parentheses) after the url of reference like

[Google][google]

[google]: https://www.google.com/  "Abc"

#### Sample:
```markdown
//Use it like this

[Google][google]

//Define it like this
[google]: https://www.google.com/ 
[google]: https://www.google.com/ "Google Search"
[google]: https://www.google.com/ 'Google Search'
[google]: https://www.google.com/ (Google Search)
[google]: <https://www.google.com/> 
[google]: <https://www.google.com/> "Google Search"
[google]: <https://www.google.com/> 'Google Search'
[google]: <https://www.google.com/> (Google Search)
```

[Back to Top](#table-of-content)

---

### Tables
Table are created using `|` (pipe) to separate columns and a combination of hyphens `-` to define the header row.  
You can align columns to **left**, **center**, or **right** by adding colons in the separator row.

#### Row Separators:
```markdown
|---------|---------|---------| //Default Left aligned

|:---------|:---------|:---------| //Use colon to align Left

|---------:|---------:|---------:| //Use colon to align Right

|:---------:|:---------:|:---------:| //Use colon on both sides to align Center
```
You can also use a combo
```markdown
| Left Align | Center Align | Right Align |
|---------|:---------:|---------:|
| Item 1 | Item 2 | Item 3 |
| Item 4 | Item 5 | Item 6 |
```
##### Output:
| Left Align | Center Align | Right Align |
|---------|:---------:|---------:|
| Item 1 | Item 2 | Item 3 |
| Item 4 | Item 5 | Item 6 |

[Back to Top](#table-of-content)

---

### BlockQuotes

Blockquotes highlight a quote or a piece of text. Use `>` to use blockquote. You can also use multiple `>` for nesting blockqoutes.
```
> This is a blockquote.  
> You can quote multiple lines.
	> Second Line
```

##### Output:
> This is a blockquote.  
>> Single Nested.
>>> Multi Nested

[Back to Top](#table-of-content)

---

### Code Blocks

If you’re adding code snippets, you can use backticks ( ` ) around a text to make it a piece of code. You can use triple backticks to add a code block. 
#### Single backtick
\` a = b \`

##### Output:
` a = b `

#### Code Block
\`\`\`
function sayHello(){
    print("Hello, world!");
}
\`\`\`

##### Output:
```
function sayHello(){
    print("Hello, world!");
}
```

You can also use keywords like ***"markdown"*** after the starting triple backticks to add colors to the code. Other Keywords include language name like ***java, javascript, dart  and kotlin*** etc.
##### Colored Code Block
\`\`\`dart
function sayHello(){
    print("Hello, world!");
}
\`\`\`

##### Output:
```dart
function sayHello(){
    print("Hello, world!");
}
```

[Back to Top](#table-of-content)

---

### Comments

If you want to leave comments in your Markdown that is possible as comments are not rendered in the output. Here are some ways to ad comments:

```markdown
Html Comment
<!-- This is a comment -->

Markdown Comment Method # 1
[//]: # (This is a comment)

Markdown Comment Method # 2
[comment]: # (This is a comment)

Markdown Comment Method # 2
[//]: # [This is a comment]
```
>  The comments will be invisible in the output.

[Back to Top](#table-of-content)

## Markdown Characters CheatSheet

| **Symbol**         | **Description**       | **Example**                    |           |                 |     |
| ------------------ | --------------------- | ------------------------------ | --------- | --------------- | --- |
| `#`                | Heading               | `# Heading 1`                  | Heading 1 |                 |     |
| `\`                | Escape                | `\# not a heading`             |           |                 |     |
| `*` or `_`         | Italic                | `*italic*`                     |           |                 |     |
| `**` or `__`       | Bold                  | `**bold**`                     |           |                 |     |
| `***`              | Bold + Italic         | `***bold italic***`            |           |                 |     |
| `- ` or `* `       | Unordered List Item   | `- Item`                       |           |                 |     |
| `1. `              | Ordered List Item     | `1. Item`                      |           |                 |     |
| `- [ ] `           | Task List (unchecked) | `- [ ] Task`                   |           |                 |     |
| `- [x] `           | Task List (checked)   | `- [x] Task`                   |           |                 |     |
| `>`                | Blockquote            | `> quote`                      |           |                 |     |
| `` `code` ``       | Inline Code           | `` `code` ``                   |           |                 |     |
| \`\`\`             | Code Block            | ```code```                     |           |                 |     |
| `[text](url)`      | Link                  | `[Google](https://google.com)` |           |                 |     |
| `![alt text](url)` | Image                 | `![alt](image.png)`            |           |                 |     |
| `<>`               | Url                   | `<https://example.com>`        |           |                 |     |
| `                  | ---                   | ---                            | `         | Table Formatter |     |
| `[//]: # (Hello)`  | Comment               | `[//]: # (Hello)`              |           |                 |     |

[Back to Top](#table-of-content)

---
## Obsidian Wiki-Links

Obsidian Wiki links are similar to the one you see in wikipedia. If you want to navigate to a specific obsidian note type the name in double brackets **`[[]]`**. Even if you don't remember the name properly you can just start typing and obsidian will show suggestion. 
This will take you to a file named markdown. If that file does not exist it will **create** a **new** one.
**`[[MarkDown]]`**
##### Output:
[[MarkDown]]

You can also use wiki links as a section link. What does that mean? Just like the [[#Links]] mentioned above it can be used to move to a specific section of the ***current markdown file*** or ***another markdown file***. 

For simple section link add a **hash(#)** before section name like `**[[#Obsidian Wiki-Links]]**`. 

##### Output:
[[#Obsidian Wiki-Links]]

For Section link to another file add fileName then a **hash(#)** and then section name like `**[[MarkDown#Table of Content]]**`. 

##### Output:
[[MarkDown#Table of Content]]
