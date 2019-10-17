# OpenImageIO-1.5.0-OCIO_win64

Hard to find windows binaries of `OIIO` built with `OCIO`

From here http://www.nico-rehberg.de/tools.html 

### Docs
https://openimageio.readthedocs.io/en/latest/oiiotool.html


### Usage
With aces `$OCIO` set

```
--ociodisplay  %s %s   Apply the named OCIO display and view (optional
                       args: from=, looks=, key=, value=)
```

Convert from acescg to Rec.2020
```
OpenImageIO-1.5.0-OCIO/bin/oiiotool.exe /d/ocio_balls/balls.exr --ociodisplay:from=acescg ACES Rec.2020 -o /d/ocio_balls/out.jpg
```
