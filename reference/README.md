# Kiran Builder Typeface

## Commands

Require

### Invert quantized images

```bash
for image in $(find . -wholename "./reference/quantized/*.png"); do convert $image -channel RGB -negate ./reference/quantized_inverted/$(basename $image);
```
