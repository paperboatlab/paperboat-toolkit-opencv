# paperboat-toolkit-opencv

The optional image-processing toolkit for [Paperboat](https://github.com/paperboatlab/paperboat):
classic image stages on `image` wires, an `Image` station object, an `image` instrument for the
Board, and three examples (`ocv-01`…`ocv-03`). It depends on OpenCV.

**Docs:** <https://paperboatlab.github.io/toolkits/opencv/>, also in the Help window (F1) of
Paperboat. Their sources live with the code: `engine/toolkit/opencv/docs/` for the toolkit's pages,
and a block's notes in its folder (`src/opencv/<block>/doc.rst`); a block's ports and params come
from the catalog, so write only what the catalog can't say.

## Install

```sh
sudo apt-get install -y libopencv-dev   # or your platform's equivalent
paperboat toolkit install opencv --repo https://github.com/paperboatlab/paperboat-toolkit-opencv.git
```

## CI

The `build` job checks out the public paperboat engine (`dev`), builds this toolkit inside it and checks
`ocv-01`. The `plugin` job installs paperboat as a release would be and runs
`paperboat toolkit install opencv --path .` against it: the toolkit as a plugin, then `ocv-01` against the SDK.
The engine's `engine/tests/opencv_test.cpp` covers the stages with synthetic Mats.
