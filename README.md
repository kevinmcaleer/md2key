# Markdown to PowerPoint conversion

This program converts simple markdown files into powerpoint presentations (that can also be opened in Apple Keynote as well as Google Slides).

Includes support for tables too.

## How to use

``` bash
pip install python-pptx markdown bs4
```

## Troubleshooting

if you're running a version of Pythion greater than 3.9 you may encounnter an error

```bash
AttributeError: module 'collections' has no attribute 'Container'
```

This can be fixed by editing the `/lib/python3.10/site-packages/pptx/compat/__init__.py` and adding the line:

``` python
import collections.abc.container
```

---

## Next steps

* [ ] Add/check for support for images too
