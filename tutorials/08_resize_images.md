## How to Resize Images from Mac Terminal

1. Open terminal

2. Navigate to folder where image is located

3. To resize individual file, maintaining aspect ratio:

`sips -Z maxsize file_name.jpg`

-Z maintains aspect ratio

maxsize takes an integer (i.e. 640), which is the maximum height and width you want your image to be (since keeping aspect ratio)

4. To resize individual file, discarding aspect ratio:

`sips -z height width file_name.jpg`

height and width also take integers (i.e 600 and 400)

5. To resize batch of images in folder:

`sips -Z maxsize *.jpg`
