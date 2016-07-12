# redux-saga-node6
This repository shows bug related to https://github.com/yelouafi/redux-saga/issues/429

The reason is that node 6 uses native generator implementation.
With simple `yield` everything works fine, but for `yield*` with takeLatest it is not.

The bug can be fixed by adding `transform-regenerator` to plugin section of `.babelrc` file.
