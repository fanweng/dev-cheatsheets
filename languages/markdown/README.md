# Markdown Syntax
## Head L2
### Head L3
#### Head L4
##### Head L5
###### Head L6

---

> Use '>' to mark reference.
> ...Continue reference...
>> Reference can be nested by using '>>'.

_This is italic text._

**This is bold text.**

**_This is bold & italic text._**

~~This is strike through text.~~

`In-line code block here`

```
// Multiple lines of code
Line 1 of code
Line 2 of code
```

```python
# syntax highlighting
def function():
    return 1

function()
```

+ Bullet list element 1
* Bullet list element 2
- Bullet list element 3

1. Numbered list element 1
2. Numbered list element 2
3. Numbered list element 3

<!--
This is a comment block which cannot be seen.
-->

| Option  | Description                        |
| ------- | ---------------------------------- |
| Table 1 | The pipeline does not have to be vertically aligned |
| Opt 2   | ... ... |
| ...     | ... ... |

[A Link](https://learn.getgrav.org/content/markdown)

[A Link with Title](https://learn.getgrav.org/content/markdown "Markdown Syntax")

![An Image with Tile](https://www.straight.com/files/v3/images/17/09/coldplay_1.jpg "Coldplay")

[Link using reference][ref_1]

![Image using reference][ref_2]

[ref_1]: https://learn.getgrav.org/content/markdown "Title here"

[ref_2]: Github_Logo.png "relative path to image"
