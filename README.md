Below are some examples of Markdown syntax which can be used with Pico:

---

`# Header1`

# Header1

---

`### Header3`

### Header3

---

`*italics*`

*italics*

---

`**bold**`

**bold**

---

`$$Insert Latex as Normal$$` (The preview won't work here)

---

`[Link text](www.google.com)`


[Link text](www.google.com)

---

To add videos:

[embed "https://youtu.be/YR12Z8f1Dh8"]

(The preview won't display this)

## Expanding Content
Adding expanding content, such as those used to hide the examples on this page, are slightly complicated to create. In particular, they require a brief dip into some real HTML.

The HTML that we particularly need is the `<details>` tag. Within it, we put the summary text (the text that doesn't get hidden) inside a `<summary>` tag.

<details markdown="1">
<summary>Example</summary>

---

``` markdown
<details markdown="1">
<summary>Click here</summary>
**Surprise!**
</details>
```
---

<details markdown="1">
<summary>Click here</summary>
**Surprise!**
</details>

---
</details>

Note that the opening tag is `<details markdown="1">`. The `markdown="1"` part allows us to use markdown (the language we normally use to specify formatting on this website) within the HTML block. Also remember that in HTML, opening tags such as `<details>` and `<summary>` must eventually be followed by their associated closing tags `</details>` and `</summary>`.

