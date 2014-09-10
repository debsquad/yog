# yog - ye old gallery

This is a quick hack to help @fluxspir organize his photos during his roadtrip
in Brazil.

Given the following structure:

```
- /home/jimmy
   - example/
      - 2014-01-01_vacation_a/
         - filea.JPG
         - fileb.jpeg
         - filec.mov
      - 2014-02-01_vacation_b/
```

And given the following invocation of yog:

```sh
yog /home/jimmy/example
```

The following would be generated:

```
- /home/jimmy
   - example/
      - 2014-01-01_vacation_a/
         - filea.JPG
         - fileb.jpeg
         - filec.mov
         + index.html
         + thumbs/
            + filea.JPG.jpg
            + fileb.jpeg.jpg
            + filec.mov.jpg
         + web/
            + filea.jpg
            + fileb.jpg
            + filec.mov
```

## Metadata
If a `metadata.txt` file is found in a folder, yog will use its content as an
introduction paragraph in the index.html.

If a file is named after a media file with a trailing `.txt` extension, it will
be used for the image title instead of the filename.

## Installation

```sh
sudo cp yog* /usr/bin
```

## Requirements
 - /bin/sh
 - ImageMagick
 - FFMpeg if you have videos in there
