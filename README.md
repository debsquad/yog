# yog - ye old gallery

This is a quick hack to help @fluxspir organize his photos during his roadtrip
in Brazil.

Given the following structure:

```
- /home/jimmy
   - example/
      - 2014-01-01_vacation_a/
         - filea.jpg
         - fileb.jpg
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
         - filea.jpg
         - fileb.jpg
         + index.html
         + thumbs/
            + filea.jpg
            + fileb.jpg
         + web/
            + filea.jpg
            + fileb.jpg
```

## Requirements
 - /bin/sh
 - ImageMagick
 - FFMpeg if you have videos in there
