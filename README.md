aperture-project-cleaner
========================

###Description
Cleans an Aperture project with separate RAW and JPG files based on RAW ratings.

If you use Aperture, and photograph both RAW and JPG, you'll perhaps feel
that it would be convenient to keep RAW files of images you like and want to
edit, and keep the JPG files of the images you just want to keep.

My review process is as follows:

1. Look at only images from either file type (only raw or only jpg)
2. Mark good images (for which I'd like to keep the raw) 4.
3. Mark mediocre image with nothing
4. Mark badly exposed or unfocused or otherwise crap images with -1 (by pressing 9)
5. Run script!
6. Delete images manually from newly created folder of reduntant images.

This script will go through a project and delete unnecessary files as follows:

Or more structured:


| Raw rating      | Jpg Rating    | Action                       |
|:---------------:|:-------------:|:----------------------------:|
| 4 ≤ r           | 0 < r ≤ 3     | del jpg                      |
| 4 ≤ r           | 4 ≤ r         | nothing                      |
| 0 < r ≤ 3       | 4 ≤ r         | set raw score to match jpg   |
| -1              | ?             | del both                     |
| ?               | -1            | del both                     |

The point is to always have a good, editable raw file for all pictures you like
and only keep the JPG if you for some reason (camera preset for instance)
like that as well, and only keep jpg:s of stuff you aren't necessarily
interested in keeping a large file for.


###Installation
Install by putting it in a script folder Aperture looks in for applescripts. Either:

`~/Library/Scripts/Aperture`

or

`/Library/Scripts/Aperture`

###Usage
You can either run the utility by opening it in Applescript Editor and pressing the run button or
enabling the applescript menu bar item and running it from there.

To enable the applescript menu bar item, open Applescript Editor and preferences, and 
check the box "Show Script menu in menu bar"

Before you run the script, make sure you have selected an image in the project you want to clean.
The script will now create an album called 'reduntant files' and add images that it feels should be cleaned out from there.

From there you can safely delete them manually.
