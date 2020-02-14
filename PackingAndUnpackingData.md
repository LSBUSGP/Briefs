# Packing and Unpacking Data

An online multi-player game requires game state data packets to be exchanged between players. The bandwidth for data transmission is extremely tight so make every byte count! You must provide functions to pack and unpack the identity, state, position, and velocity of every player, missile, and pick-up to be transmitted to the multi-player client machines. You must include a test scene which shows two views: the original host data; and the client view with object identities, states, positions, and velocities reconstructed from the packed data. You should also display the number of bytes per second required. It must be less than 4K.

![Image of a multi-player FPS](https://thelatenightsession.files.wordpress.com/2016/02/doom-xbla-split.jpg "DOOM")

You must include the following in your Unity package:

1. a script containing your data packing and unpacking functions
2. a test scene which demonstrates both a host and client view of the data
3. documentation including a formula for calculating packet size
