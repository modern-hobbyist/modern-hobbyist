Whether you have several macro keys that you can't seem to keep straight in your mind or if you want to put a picture of your dog Fufu on your keyboard's LCD, the process to do that is the same, and it's relatively simple.

# Create Your Image
This is probably the part that will take the longest, as you'll find yourself constantly tweaking the design to achieve the esthetic you're after, but the `tldr;` is that you need an image that you intend to put on your keyboard's LCD. It can be any image or even gif that you want, but for my keymap I did the following. 

1. Create an image in Photoshop that matches the LCD size (320px x 240px)
2. Add squares for all the keys I want and add the proper text
3. Adjust font, border radius, etc... to achieve the esthetic I'm going for.
4. Save the file as a PNG

# Convert Your Image
QMK and the Quantum Painter library that actually handles updating the display, can't work directly with PNG, JPEG or GIF files, so you need to convert it to a format that Quantum Painter can understand -- C code. To do that, we'll use the command line.
- In your terminal, navigate to the directory you exported your image from earlier.
  `cd ~/Desktop/mist-layouts/`
- Run the following to create the .c and .h files representing that image
  `qmk painter-convert-graphics -i <png-you-created>.png -o output -f pal4`
	- For more information on what output formats you can choose from, see [here](https://docs.qmk.fm/quantum_painter#quantum-painter-cli).
	- This will generate a `.c` and `.h` file in your output directory designated by `-o` in the command above. In this example, it will create an `output` directory inside the current working directory (`~/Desktop/mist-layouts/`)

# Compile Your Firmware
You'll next need to actually compile custom firmware for your keyboard, but if you're up for building one from scratch, I'm sure you've come across this before. I like to utilize the [Userspace](https://docs.qmk.fm/newbs_external_userspace#external-userspace-setup-locally-stored-only) functionality of QMK to keep my core `keyboard` specific code separate from my personal `keymaps`. Feel free to check out my [QMK Userspace](https://github.com/modern-hobbyist/qmk_userspace) for examples of how I configured it, but please understand I only know enough about QMK to get by, so don't take it to be a best-practice guide by any means.

- Copy the .c and .h files into your QMK userspace
	- `users/csteamengine/graphics/`
	- Feel free to use subdirectories inside `graphics` (e.g. `users/csteamengine/graphics/mist`)
- In the `rules.mk` file for your keymap, you'll have to tell qmk to compile your .c file along with the source files. Add the following line to `rules.mk`
	- `SRC += ./graphics/mist/layer-1.qgf.c`
- In your `keymap.c` file, include the `.h` file, create a variable to store the `.c` image, then load the actual image into that variable 

```c
// At top of `keymap.c`
#include "./graphics/mist/layer-1.qgf.h"
...

// At top of `keymap.c` or wherever you co-locate variables. 
static painter_image_handle_t layer_1;
...

// inside `keyboard_post_init_keymap()`
layer_1 = qp_load_image_mem(gfx_layer_1);
...

// Inside `keyboard_post_init_keymap()` or helper function of your own creation
// Feel free to update the location that you render the image
if(layer_1 != NULL) {
	qp_drawimage(lcd, 0, 25, layer_1);
}
```

# Enjoy!
That should be all you need to do to get a custom image on your LCD, whether it be a custom keymap or a photo of your kids!
