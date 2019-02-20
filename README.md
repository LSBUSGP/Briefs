# Briefs

- [Old Money System](#old-money-system)
- [Edge Detection Shader](#edge-detection-shader)
- [Score Ten Pin Bowling](#score-tep-pin-bowling)
- [Name Generator](#name-generator)
- [Offline Ranking Table](#offline-ranking-table)
- [Image Compositing Shader](#image-compositing-shader)
- [Hit a Moving Target](#hit-a-moving-target)
- [Audio Frequency Detector](#audio-frequency-detector)
- [Pattern Shuffle](#pattern-shuffle)
- [Packing and Unpacking Data](#packing-and-unpacking-data)

## Old Money System

Create a monetary system for a game based in British history before decimalisation. You need to be able to represent monetary value in terms of [£sd](https://en.wikipedia.org/wiki/£sd). You must create a class in csharp to represent amounts with functions to: add and subtract amounts; and, test if one amount is equal to, or greater, or less than another amount. You must provide a test program to demonstrate these features. You must also include the documentation needed to use your system.

![Image of old coins](http://projectbritain.com/money/images/coins.jpg "Old money")

You must include the following in your Unity package:

1. required scripts and assets
2. example scene files and test assets
3. documentation

## Edge Detection Shader

Create a post-processing effects filter to create an illustrated art look to the rendering in a game. You must create a shader that performs edge detection and highlights edges. The thickness and colour of the highlight must be shader parameters. You must provide the shader asset and any materials needed to make it work, a test program demonstrating the shader, and full documentation.

![Image of a game using an edge detection shader](http://i.imgur.com/AC1ZSeV.png "example of edge detection for drawing outlines")

You must include the following in your Unity package:

1. required shader and assets
2. a scene demonstrating the shader with adjustable parameters
3. documentation

## Score Ten Pin Bowling

Create the scoring system for a game of [ten-pin bowling](https://en.wikipedia.org/wiki/Ten-pin_bowling) using traditional scoring rules. You must accept as input, a sequence of numbers in binary code representing the pins knocked down in each frame of the game, and return the frame score for each frame you can score so far, and a symbol to place in the score sheet for the first and second roll in each frame. The first 10 bits of the input represent whether the given pin was knocked down with 1 representing down and 0 as still up. The 11th bit will be set if a foul was made. The output symbols are the digits `1` to `9`, the unicode characters `①` to `⑨` (unicode 2460 to 2468) to indicate a split, `-` for a miss, `/` for a spare, `X` for a strike, and `F` for a foul. In the last frame you must also return the possible bonus ball symbols.

![Image of a complete scored game of ten pin bowling](http://slocums.homestead.com/files/scrsheet.gif "example score")

You must include the following in your Unity package:

1. required scripts
2. an example scene different scoring scenarios
3. documentation

## Name Generator

A space exploration game requires a star system name generator to randomly create 100 billion names. The names must all be pronounceable, avoid any obscenities, and there must be no duplicates. You must provide additional programs to test your results against these restrictions.

![Image of a galaxy](https://upload.wikimedia.org/wikipedia/commons/c/c3/NGC_4414_%28NASA-med%29.jpg "galaxy")

You must include the following in your Unity package:

1. name generator script
2. duplicate checking script
3. obscenity checking script
4. an example showing a sample of generated names
5. documentation

## Offline Ranking Table

A single player arcade game requires the generation of offline ranking tables showing the top 5 places for 60 different game levels. Each level has an expected average score and [standard deviation](https://en.wikipedia.org/wiki/Standard_deviation). As input you will take a list of three letter initials (you may randomly pick from the list to populate the rankings) a list of 60 average scores and 60 standard deviations. The generated scores must be integer value multiples of 10 distributed over the range and stored in a persistent file when the program first runs. You will also receive three letter initials and scores from players as they play the game. These scores should be sorted into their correct place in the rankings and overwrite those stored in the persistent file.

![Image of an arcade game high score table](http://www.howdesign.com/wp-content/uploads/arcade-high-scores1.jpg "high score table")

You must include the following in your Unity package:

1. ranking table generator script
2. a scene to reset the ranking tables
3. an example program allow generated ranking tables to be viewed
4. a test scene where new scores can be added
5. documentation

## Image Compositing Shader

A game requires the ability to place the player's live image into the game's world. The game requires that the player sits in front of a green or blue screen so that their image can be composited into the game's graphics. A shader is required to compose the player's portrait with a game supplied background image. The game must be able to customise the colour and tolerance of the colour key removal. The shader must work with any supplied image source but should demonstrate the functionality by using the live feed from an attached web cam.

![Image of a game embedding the player's picture]()

You must include the following in your Unity package:

1. image compositing shader and customising scripts
2. a scene compositing feed from the webcam and another texture
3. documentation

## Hit a Moving Target

A 2D top down game with enemy AI needs a targeting system to shoot at the player. The shots are not instant so the system will need to aim ahead of the player's current position. Shots aimed at the player should hit if the player is not moving, or if the player is moving at a constant speed. To avoid hits, the player must need to change while the shot is travelling. As input to the system you will be given the player's relative location and velocity. You must return the relative clockwise angle in degrees needed to hit the player.

![Image of a 2D top down tank game](https://www.mobygames.com/images/shots/l/205949-wii-play-wii-screenshot-aim-your-tank-with-the-wii-remote.jpg "2D game")

You must include the following in your Unity package:

1. enemy AI targeting script
2. an example program with a sample enemy shooting at a moving player
3. documentation

## Audio Frequency Detector

A rhythm based music game requires a script to generate level data from music tracks. You must provide a script that can detect 4 distinct frequencies from the currently playing music track. Include an example scene that shows or hides 4 boxes when the frequencies are present in the music. The frequencies to detect and the thresholds should be configurable in the Inspector.

![Image of an audio based racing game](https://www.mobygames.com/images/shots/l/280862-audiosurf-windows-screenshot-avoid-the-grey-blocks-and-grab.jpg "Audiosurf")

You must include the following in your Unity package:

1. audio frequency detecting script
2. an example audio track (Creative Commons)
3. an example program to show frequency detection
4. documentation

## Pattern Shuffle

A puzzle game requires a script to semi-randomly shuffle its game pieces. Each shuffle should mix the components given and be as unpredictable as possible, but should also avoid repetition of the same piece in subsequent shuffles. For example, the first 4 components of a new shuffle shouldn't contain the last 4 components of the previous one. The number of components in the list and the limit on repeating values must be customisable through the `Inspector`.

You will be provided with a list of integers representing the individual components. You must return a new shuffle each time the `Shuffle` function is called. You must additionally provide a program to test the shuffle function to ensure that it meets the repetition requirements. This test must also include a demonstration test case to show that it can catch errors.

![Image of a puzzle game with different puzzle pieces](https://www.focuseducational.com/images/user/fullsize/shapes.jpg "puzzle pieces")

You must include the following in your Unity package:

1. a script containing the shuffle function
2. a test script and scene that stress-tests the function
3. a scene that demonstrates the test program can catch errors in sequences
4. documentation

## Packing and Unpacking Data

An online multi-player game requires game state data packets to be exchanged between players. The bandwidth for data transmission is extremely tight so make every byte count! You must provide functions to pack and unpack the identity, state, position, and velocity of every player, missile, and pick-up to be transmitted to the multi-player client machines. You must include a test scene which shows two views: the original host data; and the client view with object identities, states, positions, and velocities reconstructed from the packed data. You should also display the number of bytes per second required. It must be less than 4K.

![Image of a multi-player FPS](https://thelatenightsession.files.wordpress.com/2016/02/doom-xbla-split.jpg "DOOM")

You must include the following in your Unity package:

1. a script containing your data packing and unpacking functions
2. a test scene which demonstrates both a host and client view of the data
3. documentation including a formula for calculating packet size
