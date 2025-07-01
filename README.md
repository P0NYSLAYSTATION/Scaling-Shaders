Resizer allows you to freely crop an area of the screen, downscale only that area, and optionally then upscale it to a size of your choosing, using either linear or point filtering. 
It is intended primarily for situations where you need to scale down the image while maintaining a native resolution, and/or remove or replace pillarboxing and letterboxing that is part of the original content.

Currently it assumes that the content you want to crop to is already centered. 
I may update it at some point to allow for selection of any area and repositioning to any area, or at least to the center. If I can be bothered.
I don't really know why someone would need to do that, but probably someone out there does.

HOW TO USE:

- Set the content resolution to the size of the part of the screen you want to crop down to, for example 1440x1080 if you want a 4:3 section of a 1080p frame.
- Set the intermediate resolution to the resolution you want to downscale the cropped area to.

- Set the final resolution to the resolution you want to upscale the image back to. I recommend using an integer multiple of the downscale resolution for clean results.

The shader defaults to point filtering, but you can change this to linear in the preprocessor definitions if you want smoothed results.


EXAMPLE:

A game uses a 1080p, 16:9 framebuffer, but is pillarboxed to 4:3, and you want to play it at 640x480 for whatever reason, and you want to display that 480p image at 2x scale.
You would do the following:

- Set the content resolution to 1440x1080.

- Set the intermediate resolution to 640x480.

- Set the final resolution to 1280x960.
