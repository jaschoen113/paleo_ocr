---
title: "How to crop multiple images at once through the command line"
date: April 20 2018  
---

Adapted from [Linux Academy](https://linuxacademy.com/blog/linux/cropping-multiple-images-the-same-way-short-tutorial/)

1. Make sure that you have Gimp installed; if that's not the case, install it with the command:

	> `sudo apt-get install gimp`

2. Make sure that you have Imagemagick installed; if that's not the case, install it with the command:

	> `sudo apt-get install imagemagick`

	- Note: if that doesn't work, you will probably need to download a package from the [IM website](http://www.imagemagick.org/download/).

1. Place all the images in the same folder.

2. Open one of the images in Gimp.

3. Press R to invoke the "rectangle selection" tool; select the area that you want to crop.

4. Make sure that the "Tool Options" window is visible (to toggle it, go to the "Windows" menu, and select "Tool Options" from the "Dockable Dialogs" submenu).

5. In the "Tool Options" window, find the four fields for "Position" and "Size"; take note of the four values.

	- The former two values (under "Position") indicate the position of the __upper left corner__.
	- The latter two values (under "Size") indicate the width and height of the rectangle (in pixels).

6. Open the terminal; use "`cd`" to move to the folder where your images have been saved.

7. Type the following command:

	> `for i in $(ls *.jpg); do convert -crop {width}x{height}+{X}+{Y} $i cropped_$i; done`

	- Where, of course, "width," "height," "x," and "y" are the values that you jotted down from Gimp; while "*.jpg" corresponds to the extension of the image files that you have saved in your folder. (__Do not include the curly brackets!__)

	- __Note__: if you don't want to create cropped copies of your original files, but simply replace them, you can use this command: `mogrify -crop {width}x{height}+{X}+{Y} *.jpg`.

8. There you go! Now you all the images should have been copied and cropped into new "cropped_*.jpg" files.

- __Note__: these values seem to _generally_ work for the CC MS 198: __3750x5200+880+900__.
