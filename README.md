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

## Requirements
 - /bin/sh
 - ImageMagick
 - FFMpeg if you have videos in there
