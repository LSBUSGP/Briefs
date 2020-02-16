# Instanced Scrolling Material

A script is required to scroll a tile-able texture to give the appearance of liquid flowing. The speed and direction of the scrolling must be parameters and the speed must be independent of the frame rate. (Hint: use `Time.deltaTime` to keep the speed consistent and independent of the frame rate.)

![water uv animation](https://danlaukat.files.wordpress.com/2014/12/waterfall.gif)

You must include the following in your Unity package:

1. the required script
2. any required prefabs
3. a scene to demonstrate texture scrolling
4. documentation for this component

## Extra Credit

For extra credit on this brief, replace the material with a material instance so that the original material file is not modified. This allows multiple instances of the same material to exist with the same scene scrolling in different directions at the same time.
