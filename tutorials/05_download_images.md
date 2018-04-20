---
title: "How to download multiple images at once from the command line"
date: April 20 2018
---

- Method One; works when all images are indexed on a single webpage

	1. Find the web address of the remote webpage where all the images are indexed; in the case of the CC MS 198, the page is this one: (http://image.ox.ac.uk/images/corpus/ms198/)[http://image.ox.ac.uk/images/corpus/ms198/].

	2. Open the terminal. Use "`cd`" to move to the folder where you would like these images to be downloaded.

	3. Enter this command: 

		> ` wget --force-html -i [website]`

		- Where `[website]` is the index page that you have identified in step 1.

	4. That should work. You can get rid of unwanted files by using the command "`rm`," followed by wildcards if necessary.
