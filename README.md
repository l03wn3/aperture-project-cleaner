aperture-project-cleaner
========================

##Description

Cleans an Aperture project with separate RAW and JPG files based on RAW ratings.

If you use Aperture, and photograph both RAW and JPG, you'll perhaps feel
that it would be convenient to keep RAW files of images you like and want to
edit, and keep the JPG files of the images you just want to keep.

This script will go through a project, delete RAW files you've rated lower than 4
(but keep the corresponding JPG file), keep the RAW files you've rated 4 and higher
(and delete the corresponding JPG file) and delete both the RAW and the JPG of an image
you've rated -1.

#Installation

Install by putting it in a script folder Aperture looks in for applescripts. Either: 
`~/Library/Scripts/Aperture`
or
`/Library/Scripts/Aperture`

#Usage

You can either run the utility by opening it in Applescript Editor and pressing the run button or
enabling the applescript menu bar item and running it from there.

To enable the applescript menu bar item, open Applescript Editor and preferences, and 
check the box "Show Script menu in menu bar"

Before you run the script, make sure you have selected an image in the project you want to clean.
The script will now create an album called 'duplicates' and add images that it feels should be cleaned out from there.

From there you can safely delete them manually.