Tilemap Extractor (BMP & PNG to XPM)

My very first project to share.

This project extracts tiles from a tilemap image (BMP or PNG), resizes them, and converts them to the XPM format.
It is useful for converting sprite sheets into individual XPM tiles, supporting transparency for PNG files.

Features
✅ Extracts tiles from a tilemap (BMP or PNG)
✅ Resizes each tile to a specified size
✅ Converts tiles to XPM format
✅ Supports transparency for PNG images
✅ Automatically generates unique color symbols for XPM

Installation
This project requires SDL2 and SDL2_image

On Debian/Ubuntu:
```sudo apt install libsdl2-dev libsdl2-image-dev```

On macOS (with Homebrew):
```brew install sdl2 sdl2_image```

How to use:
```Make``` to compile and create the folders.
Put the tilemap in the main directory.
```Make fclean``` to remove all the tiles extracted.


Run the program with:
```./tile_extractor <tilemap.format> <tile_width> <tile_height> <output_tile_size>```

Example:
```./tile_extractor tileset.png 32 32 16```
This will extract 32x32 tiles from tileset.png, resize them to 16x16, and save them in extracted/ as .xpm files.

Extracted tiles are saved as:
extracted/tile_X_Y.xpm
where X and Y are the tile positions in the original tilemap.

Notes
The programm doesn't handle gaps in tilemap. 
The program automatically creates the "extracted" folder if it doesn't exist.
Supports both BMP and PNG as input formats.
The XPM output is suppose to includes color mapping and transparency.
