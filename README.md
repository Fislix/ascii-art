Simple command line [ASCII art](https://en.wikipedia.org/wiki/ASCII_art "Wikipedia article") generator inspired by [this tutorial](https://robertheaton.com/2018/06/12/programming-projects-for-advanced-beginners-ascii-art/).

### Usage
Running this program with `--help` will show you how to use this tool:

```
Usage: ascii_art.exe [OPTIONS] <FILE_PATH>

Arguments:
  <FILE_PATH>
          Path to an image file

Options:
  -s, --scale <SCALE>
          The factor by which to scale the image before transforming it to ASCII art

  -W, --width <WIDTH>
          Width to scale the image to. If no value is provided for height, this preserves the aspect ratio

  -H, --height <HEIGHT>
          Height to scale the image to. If no value is provided for width, this preserves the aspect ratio

  -m, --method <METHOD>
          Method to be used to determine the brightness (and thus the corresponding ASCII character) of a pixel

          [default: luminosity]

          Possible values:
          - average:
            Average of the red, green, and blue values
          - lightness:
            Average of maximum and minimum values out of the red, green, and blue values
          - luminosity:
            Weighted average of the red, green, and blue values to account for human perception

  -i, --invert
          Inverts the brightness

  -c, --chars-per-pixel <CHARS_PER_PIXEL>
          Number of chars to be printed for one pixel to account for non-square shape of characters vs square shape of pixels

          [default: 2]

  -r, --ramp <CHARACTER_RAMP>
          A string of characters to map the different brightness levels to. Sorted in ascending order (by "density")

          [default: " .,-:=+*/?#%@"]

  -h, --help
          Print help (see a summary with '-h')
```