---
title: "How to add an image to a markdown file"
date: May 2018
---

1. Find and copy the URL for the image that you want to add to the .md file (go to the webpage where the image is stored, right-click on the image, select "Copy image address").

    - Example:
    > `https://github.com/gesaretto/paleo_ocr/blob/master/images/p_with_ri.png?raw=true`

2. In the .md file, copy paste the URL address; put it in parentheses. Add a description of the image in quotes, after the URL (this will appear in stead of the text, or as a caption when one places the cursor over the image).

    - Add the text "`[alt text]`" (including the square brackets) before the URL and caption text in parentheses. Add an exclamation mark before the first square bracket.

    > `![alt text](https://github.com/gesaretto/paleo_ocr/blob/master/images/p_with_ri.png?raw=true "P with 'ri' abbreviation")`
