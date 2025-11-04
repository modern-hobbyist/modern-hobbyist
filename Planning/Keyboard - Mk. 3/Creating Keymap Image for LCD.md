- Create an image in Photoshop that matches the LCD size (320px x 240px)
- Add squares for all the keys I want and add the proper text
- Save the file as a PNG
- Navigate to that directory in the Terminal
- Run the following to create the .c and .h files representing that image
	- `qmk painter-convert-graphics -i <png-you-created>.png -o output -f pal4`
- Copy the .c and .h files into my QMK userspace
	- `users/csteamengine/graphics/`
	- Feel free to use subdirectories inside `graphics`
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


