# Connected-component labelling (aka blob extraction)
### by Andrew Brampton 2011

Simple javascript library that does connected-component labelling (aka blob
extraction). It uses the Algorithm described in the paper "A linear-time 
component labeling algorithm using contour tracing technique".

This is useful for Computer Vision problems, such as identifying objects in
a photo.

## Usage:

    <script type="text/javascript" src="connected-component-labelling.js"></script>

    <script>
        matrix = BlobExtraction(matrix, rect);
    </script>

## API:
    function BlobExtraction(matrix, width, height)

Performs blob extraction on a matrix of zeros and ones. The matrix must be a
one dimensional array, which represents a image with dimisions width x height.

A array the same size as matrix is returned, containing numbered labels.

    function BlobBounds(labels, width, height)

Uses the labels returned by  BlobExtraction, works out the bounds of each labelled blob.

    function BlobColouring(dest, width, height, labels)

Creates a coloured image, containing all the blobs identified in labels.

# Licence (Apache 2)

```
Copyright 2021 Andrew Brampton All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
