# Hit a Moving Target

A 2D top down game with enemy AI needs a targeting system to shoot at the player. The shots are not instant so the system will need to aim ahead of the player's current position. Shots aimed at the player should hit if the player is not moving, or if the player is moving at a constant speed. To avoid hits, the player must need to change while the shot is travelling. As input to the system you will be given the player's relative location and velocity. You must return the relative clockwise angle in degrees needed to hit the player.

![Image of a 2D top down tank game](https://www.mobygames.com/images/shots/l/205949-wii-play-wii-screenshot-aim-your-tank-with-the-wii-remote.jpg "2D game")

You must include the following in your Unity package:

1. enemy AI targeting script
2. an example program with a sample enemy shooting at a moving player
3. documentation
