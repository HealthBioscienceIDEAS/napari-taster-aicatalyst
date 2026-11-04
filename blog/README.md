## Export and view the tutorial

The tutorial is written in `blog/napari-microsam-tutorial.ipynb`, to export this to HTML, from the `blog/` folder run:

```bash
uv run --with "nbconvert>=7.16,<8" jupyter nbconvert --to html --embed-images napari-microsam-tutorial.ipynb
```

This creates `napari-microsam-tutorial.html`, which you can open in your browser by double-clicking it.