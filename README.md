## Wedding Homepage

See [index.md](index.md) for actual page source, this [URL][the_marriage] for
the rendered page.

[the_marriage]: https://mookerzhou.github.io/the_marriage/

## Misc.

### FFMPEG Instructions

Rough instructions to render GIF from iPhone video:

```bash
$ ffmpeg -i IMG_9280.MOV -ss 00:00:10 -to 00:00:13.6 IMG_9280.trimmed.mov
$ ffmpeg -i IMG_9280.trimmed.mov -vf "fps=10,scale=240:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" -loop 0 IMG_9280.trimmed.gif

$ ffmpeg -i IMG_5450.mov -ss 00:00:12 -to 00:00:17 IMG_5450.trimmed.mov
$ ...
```

### Render Locally

Using [grip](https://github.com/joeyespo/grip):

```
$ grip index.md
```
