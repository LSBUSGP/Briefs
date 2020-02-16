# Shader Variant Generator

Modern games require the generation of many variant versions of each custom shader you supply. Unity will automatically generate a superset of all the possible variations it might need for your project. This can waste gigabytes of memory, and slow both load times and build times. (On a recent project our build machine took almost 3 days to complete a build of every potential shader variant.)

Fortunately Unity includes a method to strip unwanted shaders from the build process. Unfortunately, you must manually create a file of all the specific shaders you want to preserve. A script is required to help generate this list.

Your script must take a list of lists as inputs. Each list represents one aspect of variation. Your script must then generate a list of all the unique combinations of those variations. For example, given the following three lists:

- `(DIRECTIONAL, POINT)`
- `(LIGHTMAP_ON, LIGHTMAP_SH, null)`
- `(FOG_LINEAR, null)`

each containing a list and where `null` represents an empty string. The script should produce all of the following valid output combinations in any order:

``` none
DIRECTIONAL LIGHTMAP_ON FOG_LINEAR
DIRECTIONAL LIGHTMAP_ON
DIRECTIONAL LIGHTMAP_SH FOG_LINEAR
DIRECTIONAL LIGHTMAP_SH
DIRECTIONAL FOG_LINEAR
DIRECTIONAL
POINT LIGHTMAP_ON FOG_LINEAR
POINT LIGHTMAP_ON
POINT LIGHTMAP_SH FOG_LINEAR
POINT LIGHTMAP_SH
POINT FOG_LINEAR
POINT
```

In general the output should produce a number of combinations equal to the product of the length of each list. In the above example `2*3*2`, that is 12 possible combinations.

You must include the following in your Unity package:

1. the required scripts
2. documentation for this component

## Extra Credit

Write the output of this script into a `.shadervariants` asset. See the [ShaderVariantCollection](https://docs.unity3d.com/ScriptReference/ShaderVariantCollection.html) class for more details.