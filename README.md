# font2sif
This tinny Python utility converting TrueType/OpenType/WOF Fonts to SIF (System Independent Font) format (namely used by emWin embedded GUI and a like).
The utility supports bit depth (1,2,4bpp), range selection and PNG rendering of preview image of all included characters.

## Why?
Most embedded devices do not support vector-based fonts.
Those has to be rendered in advance to pixel format.
Guess what? Tools to do that are not freely provided with embedded libraries.

## Example

```sh
python3 font2sif.py --help
```

```sh
python3 font2sif.py --path Saira-Regular.ttf --size 36 --bpp 2
```
You can pick character ranges to include, or characters to exclude, reducing the size
```sh
python3 font2sif.py --path Saira-Regular.ttf --size 36 --ranges 0x0020:0x007E 0x0090:0x0A00 --exclude 0x00AA 0x00BB
```

## Thanks
Thank to guys from https://www.freetype.org/ they provide the actual rendering engine, making it all possible.
