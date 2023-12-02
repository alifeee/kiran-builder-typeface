# Kiran Builder Typeface

## Commands

Require

### Invert quantized images

```bash
for image in $(find . -wholename "./reference/quantized_png/*.png"); do convert $image -channel RGB -negate ./reference/quantized_inverted_png/$(basename $image);
```

### Convert quantized images to bitmaps

```bash
for image in $(find . -wholename "./reference/quantized_inverted_png/*.png"); do convert $image ./reference/quantized_inverted_bmp/$(basename ${image%.*}).bmp; done
```

### Trace bitmaps with `potrace`

```bash
for image in $(find . -wholename "./reference/quantized_inverted_bmp/*"); do potrace --svg $image -o "./reference/traced/$(basename ${image%.*}).svg"; d
one
```
