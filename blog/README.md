## View the tutorial

You can [**view the image analysis with napari tutorial in your browser**](https://htmlpreview.github.io/?https://github.com/HealthBioscienceIDEAS/napari-taster-aicatalyst/blob/sp/aibio_blog/blog/napari-microsam-tutorial.html).

## Export the tutorial to HTML

The tutorial is written in `blog/napari-microsam-tutorial.ipynb`. To export it to HTML, run the following command from the `blog/` folder:

```bash
uv run --with "nbconvert>=7.16,<8" jupyter nbconvert --to html --embed-images napari-microsam-tutorial.ipynb
```

This creates `napari-microsam-tutorial.html`, which you can open in your browser by double-clicking it.