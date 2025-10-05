Minecraft Geoguessr (425 points, 4 solves)
misc★★★★★
 
Author: apple, Mystiz


Description:
Do you know Rainbolt? If you send him a photo, he could immediately tell you where it was taken in.
Can you do the same in the Minecraft world?
Note: If you are desperate, you can watch Rainbolt's most insane geoguessr moments, or LiveOverflow's video series on Minecraft Hacking.
By the way, the map is generated with Minecraft 1.17.1. With that said, you may be unable to look for the better caves.
minecraft-geoguessr_92102d07609feffc12de1372b3124552.png
https://minecraft-geoguessr.hkcert22.pwnable.hk/

Analysis:
Known Details:
An in-game screenshot with a plains biome, and a taiga biome close by, all next to a river biome.
Clouds are visible from the screenshot, which may be useful for coordinates cracking.
The resolution of the image is relatively high, clear block patterns can be seen.
 
Tips:
If you are new to finding Minecraft coordinates through screenshots, you can refer to this discord server which discovered the pack.png seed:
https://discord.gg/mch


Solution: (Spoilers)
In Minecraft, there are some blocks that have texture orientation dependent on the x, y, z location of the block. Some of those include Grass Blocks, Sand, Gravel, etc. The orientation of these blocks are universal around all seeds, and it can be manipulated to search for the exact coordinates of images, especially if you know the range of the image taken.

Through the help of 19MisterX98, you may find their Github project: https://github.com/19MisterX98/TextureRotations, which can help you dial in the relative coordinates and orientations of each block.
 
(a picture by Mystiz which laid out some of the grass block orientations)

With this image alone, it is already possible to decode the location of the screenshot, but would still take some time to run through all possible results. To minimize the time, we may try and find the y coordinates of the (0, 0, 0) defined in the picture.

Looking at the image, you would be able to see a river biome not far away from the nearest patch of grass. By viewing the Minecraft Wiki (or source code if you want to be fancy), the sea level is set to a default of 62. (https://minecraft.fandom. com/wiki/Altitude).

By counting up the y-levels, we may choose one of the blocks as the starting position, and loop through all the possible outcomes in that y-level, so that we can further reduce the runtime of the program.



An additional thing to mention, is when performing simple boundary tests, you will find out that the coordinates are restricted to this limit:
 
As shown, we can further limit the program to only search for blocks between:
x (-  [-20000, 20000]
y = <insert found y-position here>
z (-  [-20000, 20000]

As for the direction of the player, we can simply bruteforce it by trying all rotations.

If you insist on finding the actual rotation of the screenshot, you may use the cloud patterns to try and find the rotation. However, since there are only 4 possible cardinal directions, it is not advised to spend extra time in finding the direction of the blocks. 
