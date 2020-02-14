# Score Ten Pin Bowling

Create the scoring system for a game of [ten-pin bowling](https://en.wikipedia.org/wiki/Ten-pin_bowling) using traditional scoring rules. You must accept as input, a sequence of numbers in binary code representing the pins knocked down in each frame of the game, and return the frame score for each frame you can score so far, and a symbol to place in the score sheet for the first and second roll in each frame. The first 10 bits of the input represent whether the given pin was knocked down with 1 representing down and 0 as still up. The 11th bit will be set if a foul was made. The output symbols are the digits `1` to `9`, the unicode characters `①` to `⑨` (unicode 2460 to 2468) to indicate a split, `-` for a miss, `/` for a spare, `X` for a strike, and `F` for a foul. In the last frame you must also return the possible bonus ball symbols.

![Image of a complete scored game of ten pin bowling](http://slocums.homestead.com/files/scrsheet.gif "example score")

You must include the following in your Unity package:

1. required scripts
2. an example scene different scoring scenarios
3. documentation
