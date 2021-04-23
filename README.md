# 6.857 final project

## Installing and running

To install dependencies:

```
pip3 install -r requirements.txt
```

Currently, all the code for the encryption scheme test implementation lives in `encrypt.py`.

## Encryption scheme
Our code implements the image encryption scheme described in [this paper](https://www.nature.com/articles/s41598-020-78127-2).

## Image compression

The Instagram compression algorithm is proprietary and seems to be platform-dependent.  For better consistency and tunable parameters, we can use this ImageMagick command:

```
convert feldroy-512x512-unoptimized.jpg \
-sampling-factor 4:2:0 \
-strip \
-quality 85 \
-interlace Plane \
-gaussian-blur 0.05 \
-colorspace RGB \
feldroy-512x512-combined.jpg 
```
([source](https://dev.to/feldroy/til-strategies-for-compressing-jpg-files-with-imagemagick-5fn9))

## Test images

`test_image_1`: https://commons.wikimedia.org/wiki/File:AsterNovi-belgii-flower-1mb.jpg (CC BY-SA 3.0)
