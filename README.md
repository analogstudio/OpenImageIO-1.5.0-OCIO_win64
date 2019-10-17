# OpenImageIO-1.5.0-OCIO_win64

Hard to find windows binaries of `OIIO` built with `OCIO`

From here http://www.nico-rehberg.de/tools.html 

### Docs
https://openimageio.readthedocs.io/en/latest/oiiotool.html
and specifically `ociodisplay`
https://openimageio.readthedocs.io/en/latest/oiiotool.html#cmdoption-ociodisplay

### Usage
With aces `$OCIO` set

``` 
--ociodisplay  %s %s   Apply the named OCIO display and view (optional
                       args: from=, looks=, key=, value=)
```

Convert linear (acescg) `exr` to sRGB `jpg` with Rec.2020 'look' applied.

So this example
 - from=`acescg` (optional inputcolorspace arg)
 - display=`ACES`
 - view=`Rec.2020`
 
```
OpenImageIO-1.5.0-OCIO/bin/oiiotool.exe /d/ocio_balls/balls.exr --ociodisplay:from=acescg ACES Rec.2020 -o /d/ocio_balls/out.jpg
```

### In theory, but I cant get it to work... Same setup works in nuke

Convert sRGB `jpg` 'texture' to a linear `exr` to display correctly when viewed at `Rec.2020`

```
OpenImageIO-1.5.0-OCIO/bin/oiiotool.exe /d/ocio_balls/balls.exr --ociodisplay:from=out_rec2020 ACES Raw -o /d/ocio_balls/out.jpg
```
