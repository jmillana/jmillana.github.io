---
layout: single
title:  "Github Pages Markdown guide"
date:   2022-10-01 12:00:00 +0200
categories: jekyll update
---
In this post we will go through the main elements in markdown supported by github pages. For more information about markdown, please visit [GitHub's markdown guide](https://guides.github.com/features/mastering-markdown/).

## Headers
```
# H1
## H2
### H3
...
###### H6
```
# Header 1
## Header 2
###### Header 6

## Emphasis
Emphasis (italics) can be achieved by enclosing words or phrases with asterisks `*` or undersocres `_`
Strong emphasis (bold) with double asterisks `**` ir underscores `__`
For strikethrou double tildes `~~` can be used

Text with *italics*, __bold__ and ~~strikethroug~~


## Lists
Ordered lists:
\1. Fist item
\2. Second item

1. First item
2. Second item

You can create unordered lists with dashes `-`, pluses `+` and asterisks `*`

 \* item 1

 \- item 2
* item 1
* item 2

And create sublists, eighter ordered and unordered by indenting it
```markdown
* Fist level
  * Unordered sub item
  * Unordered sub item
```
* First level
  * sub item 1
  * sub item 2

## Code snipets
You can add inline code with single backquote (\`) or code blocks enclosed with triple backquote (\`\`\`) like so:
<br>
Run the command \`cd pwd\`
<br>
Run the command `cd pwd`

\`\`\`bash

echo "Hello"

\`\`\`

```bash
echo "Hello"
```
Also the code sniptes can be in different programing languajes like python, bash, yaml, etc

\`\`\`python

my code here...

\`\`\`

```python
from pathlib import Path

my_path = Path("/") / "some" / "random" / "path"
```

## Links
Named links: `\[Name to display\]\(url\)`
Note that the url can be eigher to an internal or an external resource

[Jekyll docs](https://jekyllrb.com/docs/)

Unnamed links: `\<url\>`

<https://jekyllrb.com/docs/>

## Images
In order to add images add `![hover name](/path/to/the/image)`
<br>
![hypnotoad](/assets/images/githubpages_markdown/hypnotoad.webp)
<br>
If the image do not exists, the hover name will be shown.
<br>
![hover name](/assets/images/githubpages_markdown/not_found.jpg)

## Footnotes
Foot note 1\[^1]

Foot note 2 (with words)\[^note]


[^1]: Reference 1
[^note]: Some clarification

Foot note 1[^1]

Foot note 2 (with words)[^note]

[^1]: Reference 1
[^note]: Some clarification