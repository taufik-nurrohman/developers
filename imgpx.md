---
description: >-
  Imgpx is an image proxy that can be used to get every images on the web by
  providing an URL. It's fast and advanced. Imgpx also can be used to edit images on the fly.
---

# Imgpx

## Getting Started

The simplest example would be to take an optimized image file from an external URL that points to the original image (without the URL protocol):

```text
GET https://cdn.staticaly.com/img/:REMOTE_IMAGE_URL
```

This service supports several URL parameters to manipulate the image output. Example:

```text
GET https://cdn.staticaly.com/img/:REMOTE_IMAGE_URL?w=72&h=72
```

### Sizing

Parameter | Description
--------- | -----------
`w` | Set custom image width in pixels by default. Append an `%` to the image size to resize it based on percentage relative to the original image width. The format is `w=<number>` or `w=<number>%`
`h` | Set custom image height. Append an `%` to the image size to resize it based on percentage relative to the original image height. The format is `h=<number>` or `h=<number>%`
`crop` | Crop the image based in the given width, height, X and Y coordinate. The format is `crop=<x>,<y>,<w>,<h>`
`resize` | Resize and crop to the given dimensions in pixels. The format is `resize=<w>,<h>`
`fit` | Resize but keep aspect ratio to fit to the given boundaries. The format is `fit=<w>,<h>`

### Quality

Parameter | Description
--------- | -----------
`quality` | Set image quality as percentage (only for JPEG images). The format is `quality=<number>`
`strip` | Remove metadata from the JPEG image. The format is `strip=all`

### Manipulation

Parameter | Description
--------- | -----------
`lb` | Add _letterboxing_. The color code is optional (it’s black by default). The format is `lb=<w>,<h>,<color>`
`ulb` | Remove _letterboxing_ with auto-detection of the _letterbox_ color. The format is `ulb=<boolean>`
`filter` | Apply various `imagefilter` filters. The format is `filter=<name>`
`brightness` | Adjust image brightness. The format is `brightness=<number>`
`contrast` | Adjust image contrasts. The format is `contrast=<number>`
`colorize` | Remove background from the subject on image. The format is `contrast=<boolean>`
`smooth` | Smoothes out the image. The format is `smooth=<number>`
`zoom` | Resize images for high pixel ratio devices with numbers as times (`1` means zoom 1 times, `2` means zoom 2 times). The format is `zoom=<number>`
`removebg` | Remove background from the subject on image. The format is `removebg=<boolean>`

## Miscellaneous

You can also get random images with **Imgpx**:

```text
GET https://cdn.staticaly.com/img/random
```

Or get food with:

```text
GET https://cdn.staticaly.com/img/food
```

