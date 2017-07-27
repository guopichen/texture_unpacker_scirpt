TextureUnpacker
========================

# Overview
Use this script to unpack **.png** sprites from the sprite atlas (providing a **.plist** or **.json** data file and a **.png** file) packed by [TexturePacker](http://www.codeandweb.com/texturepacker/).

# Dependencies
  - [Python](http://www.python.org)
  - [Pillow (PIL fork)](https://github.com/python-pillow/Pillow) 

# Usage
	
	$ python unpacker.py <filename> [<format>]
	
## filename

- Filename of the sprite atlas image and data file without extensions.

## format 

*optional*

- Data file format. Valid values are **plist** and **json**. If omitted **plist** format is assumed.

# Examples

### Default (plist) example

We have a pair of sprite atlas files named **Sprite.plist** and **Sprite.png** packed by [TexturePacker](http://www.codeandweb.com/texturepacker/).
Put them in the same folder as the **unpacker.py** script and run one of the following commands:

    python unpacker.py Sprite
    
or

    python unpacker.py Sprite plist
    
    
Script will generate a folder named **Sprite** containing all the sprites from the sprite atlas.

### JSON example

If you have **Sprite.json** data file instead of the **Sprite.plist** one run the following command:

    python unpacker.py Sprite json
    
Result will be the same.

# 补充
若执行报错: ImportError: No module named PIL, 则需安装PIL模块:
1. 执行命令(安装pip): sudo easy_install pip
2. 如果出现错误:  'X11/Xlib.h' file not found, 则执行: xcode-select --install, 然后再执行上一步
3. 再安装Pillow模块即可：sudo pip install pillow


