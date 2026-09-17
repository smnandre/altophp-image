# Image operations

Image operations change pixels or geometry. Metadata policies are documented
separately under [Metadata and safety](metadata-and-safety.md).

## Choose a resizing operation

The same 768 by 432 source produces these outputs for a 320 by 240 box:

| Operation | Result | Use when |
| --- | --- | --- |
| [Cover](operations/cover.md) | 320 x 240, cropped | The frame must be filled |
| [Contain](operations/contain.md) | 320 x 240, padded | The entire source and fixed frame matter |
| [Fit](operations/fit.md) | 320 x 180 | Keep the whole source with no padding |
| [Resize outside](operations/resize.md) | 427 x 240 | Preserve ratio while covering the minimum dimensions |

| Cover | Contain | Fit |
| --- | --- | --- |
| ![Cropped cover](assets/examples/cover.png) | ![Padded contain](assets/examples/contain.png) | ![Ratio-preserving fit](assets/examples/fit.png) |

Geometry and encoding are separate: selecting WebP or JPEG does not select a
resize policy. The linked guides show the shared source, exact options, and
actual outputs. Smaller inputs are not enlarged by default.

## Resize

- [Cover](operations/cover.md)
- [Contain](operations/contain.md)
- [Fit](operations/fit.md)
- [Scale](operations/scale.md)
- [Stretch](operations/stretch.md)
- [Resize](operations/resize.md)

## Geometry

- [Crop](operations/crop.md)
- [Extend](operations/extend.md)
- [Trim](operations/trim.md)
- [Rotate](operations/rotate.md)
- [Flip](operations/flip.md)
- [Orient](operations/orient.md)

## Composition

- [Flatten](operations/flatten.md)
- [Overlay](operations/overlay.md)

## Effects

- [Blur](operations/blur.md)
- [Sharpen](operations/sharpen.md)
- [Adjust](operations/adjust.md)
- [Grayscale](operations/grayscale.md)
- [Invert](operations/invert.md)
- [Pixelate](operations/pixelate.md)
- [Tint](operations/tint.md)

## Colour

- [Convert a colour profile](operations/convert-colour-profile.md)

Every method returns a new `Image` or `ImageSet`. The source is unchanged.
Drivers can report an approximate result through `Result::$degradations`.
