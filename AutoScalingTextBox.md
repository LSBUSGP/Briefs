# Auto Scaling Text Box

A game UI needs to place a `sliced` background image around some game generated `Text` object. The length of the text may very throughout the game so the size of the box should re-size to fit.

![a loot drop](https://www.omgubuntu.co.uk/wp-content/uploads/2012/12/torchlight-loot.jpg)

The Unity manual [suggests](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/HOWTO-UIFitContentSize.html#fit-to-size-of-ui-element-with-child-text) you can use a combination of layout group and content size fitter. To my knowledge this does not work and never has. And as this library is now deprecated, it doesn't seem like they will ever fix it.

You must create a custom script to calculate the size of the text box required, and then re-size the parent image to fit.

You must include the following in your Unity package:

1. the required script
2. a scene demonstrating the behaviour
3. documentation for this component

## Extra credit

Allow support for both standard `Text` and `TextMeshPro` components.
