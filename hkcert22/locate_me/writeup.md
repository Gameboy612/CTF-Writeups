CTF 2022
Locate Me (150 points, 70 solves)
misc★★☆☆☆
 
Author: GonJK

Description:
What drawing? No one seems to know you!
Attachment: locate-me_f88ddb5d5df316c0e7f780cdd4cf231b.zip

Analysis:
Inside the folder, you would find a total of 297 pictures inside the pic folder, named 1-297, with jpg format.
i.e. 2.jpg, 57.jpg, 280.jpg. 

We recommend giving this puzzle a try before going to the solution, as the solution is not as complicated as you thought.

Tips:
1.	The data of each individual picture is different, even though they seem the same at first glance.
2.	When a picture is taken, a lot of different data is often stored in the file. For example, the time taken, the location taken, the modified date, the camera device data etc.

Spoilers:
Thought Process:
Upon analyzing the pictures, it is found that some of the pictures in the folder are repeated. Therefore, we can tell that the actual image of the folder is not important.
Another idea we have thought of before finding the solution, is to split the photos up to the factors of 297, notably 11 x 27, 9 * 33 and 3 * 99. However, no specific pattern can be found after arranging the files in this manner.

When we throw these pictures into autopsy, we had two main directions for finding the key. The first one being the creation date of the pictures, as the last created picture may be related to where the author is (because of the title, “Locate Me”), finding the coordinates taken during the shooting, and find it from Google Map. However, there does not seem to be any useful information in the coordinates nor the actual picture.

Another direction that we thought of, was to analyze the coordinates of all the pictures. It was found that even duplicated pictures have different coordinates. With this new found knowledge, we tried to plot all the different picture coordinates into a map, hopefully seeing some sort of pattern.

[Link to how to plot coordinates into Google Maps (My Map) via Google Photos]


TL;DR Solution:
1.	Upload all the images to three separate Google Photos Album. (Because of the limit of google maps only allowing 100 locations per layer)
2.	Upload the 3 albums to Google Maps (My Map)
3.	Read the pattern.
