# Markdown to PowerPoint conversion

This program converts simple markdown files into powerpoint presentations (that can also be opened in Apple Keynote as well as Google Slides).

Includes support for tables too.

## Example markdown file:

```markdown
# This is the first slide

## this is a subtitle

* some text 1
* some text 2
* some text 3
  * indented text

# This is the second slide

**A table**

item   | Description  | Qty |  Price
-------|--------------|:---:|------:
item 1 | its an item  |  1  | £12.00
item 2 | another item |  2  |  £0.99
```

## Dependencies

* You'll need to install the `python-pptx`, `markdown` and `beautiful soup` libraries.

``` bash
pip install python-pptx markdown bs4
```

---

## How to use

Run the program with two parameters; the name of the markdown file and the name of the file to output to:

``` bash
python md2pptx test.md test.pptx
```

You can then open the `test.pptx` file in your favourite presentation software and apply a theme of your choosing.

---

## Troubleshooting

if you're running a version of Pythion greater than 3.9 you may encounnter an error

```bash
AttributeError: module 'collections' has no attribute 'Container'
```

This can be fixed by editing the `/lib/python3.10/site-packages/pptx/compat/__init__.py` and adding the line:

``` python
import collections.abc
```

---

## Next steps

* [ ] Add/check for support for images too
