# LIFE Biota wide pack

Offline species-identification data pack used by the LIFE mobile app (Biota). The app downloads these five files, verifies each against a pinned SHA-256 and refuses anything that does not match. Do not use these files standalone; they are in a LIFE-specific int8 layout.

Biota geniş paketi: LIFE uygulamasının çevrimdışı tür tanıma verisi. Uygulama beş dosyayı indirir ve sabit SHA-256 ile doğrular.

| File | Size (bytes) | SHA-256 |
|---|---|---|
| names.jsonl | 84646534 | 6ddfa885fffc5b56fb3483ff8c909ffd02e939eefe65d706431e534cfa02d501 |
| offsets.u64 | 6939648 | c3beecf7c2357808a1b56ba0e82ff95ffa292dfba7d205f71f4e9044470f3aeb |
| scales.f32 | 3469820 | 63b880ff8b94cb87bcb125c1bf65a3d0840a4137f17bedbc1f16d99328648ab3 |
| vectors.i8 | 666205440 | e1d59d4be4e077ad5f9749f25de2ad585e2c43b82530ff1cf65bd4b6ffe08516 |
| vision_int8.onnx | 309374410 | 22c8d0f678c5c85b67d5c4425c4695127af56253f5ad9c1071c4a3b14daa0898 |

## Provenance and licences

- `vision_int8.onnx`: int8-quantised image tower of [BioCLIP 2](https://huggingface.co/imageomics/bioclip-2) (MIT).
- `vectors.i8`, `scales.f32`: int8-quantised BioCLIP 2 text embeddings of the species list in [TreeOfLife-200M](https://huggingface.co/datasets/imageomics/TreeOfLife-200M) (revision `5f2dc493b3dc0e544438a04038ab15faa646b749`; compilation marked CC0 1.0).
- `names.jsonl`, `offsets.u64`: 867,455 species labels (7-rank Linnaean names and one common name) from the same dataset revision; common names originate from the GBIF Backbone `VernacularName` component.
- No images from TreeOfLife-200M are included.

BioCLIP 2: Gu et al., arXiv:2505.23883 (2025). BioCLIP: Stevens et al., CVPR 2024.

### MIT notice (BioCLIP 2, github.com/Imageomics/bioclip-2)

```
Copyright (c) 2023-2026 Imageomics Institute
Copyright (c) 2024-2025 Samuel Stevens
Copyright (c) 2022 sgvaze
Copyright (c) 2021 Visipedia
Copyright (c) 2012-2021 Gabriel Ilharco, Mitchell Wortsman, Nicholas Carlini,
Rohan Taori, Achal Dave, Vaishaal Shankar, John Miller, Hongseok Namkoong,
Hannaneh Hajishirzi, Ali Farhadi, Ludwig Schmidt

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
