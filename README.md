# happymeal
Simple Python script for cafeterias and canteens managed by the Studentenwerk Lower Saxony 

This Script provides you with basic Settings for commonly used canteens (Mensa 1, Mensa 2, Mensa 360) see `mensa --help` for choices

# Installation

## Prerequisites
python3 urllib, datetime, timedelta, argparse, xml.etree.ElementTree

`pip install -r requirements.txt`

The script needs to be placed somewhere covered by your bash/python PATH, typically everythinh in `/home/`, `/usr/bin/` or `/usr/local/bin/` should do the trick

## For casual users:
If you are not that familiar with Linux, copy the mensa file into `/usr/local/bin/`

# Usage
To start simply run `mensa` in your Terminal the canteen selected will default to [Mensa1](https://www.stw-on.de/braunschweig/essen/mensen-cafeterien/mensa-1/)

## optional usage

### selection of mealtype
The selection of food defaults to list everything, but you can change it with the `-m` flag
* To select only vegetarian (vegan included) add the `-m vet` flag to the script call
* To select only vegan meals add the `-m veg` flag to the script call

### selection of date
At this point the script can only show meal of today and tomorrow defaulting to today, but you can change it with the `-d` flag
* To see which meals await you tomorrow, simply add the `-d tom` flag to the script call

### selection of canteen
At this point there are only three canteens included, but changes are easy to be accomplished. Since the ID of a canteen is not the same as the name as it is known, it has to be defined in script, or you need to look it [up](http://api.stw-on.de/xml/mensa.xml) which can be hard, that's why I included the top 3 canteens for TU Braunschweig. You can change the id with the `-id <id>` flag, defaults to mensa 1.
* To see what's cooking at the 360, simply add the `-id 360` flag to the script call
* To see what's cooking at Mensa 2, simply add the `-id 2` flag to the script call
* To see what's cooking at Mensa 1, simply add the `-id 1` flag to the script call

### Changing the colour output
The script includes a `colourize_rows` function, which uses `\033[38;5;#m` for the text in the foreground and `\033[48;5;#m` for the background
Or something like `\033[38;5;#;48;5;#m` to set both 
Where # is an 8-bit code, resulting from this [table](https://web.archive.org/web/20131010034437im_/http://bitmote.com/public/8-bit_color_table.png).
You can simply change values to your favourized colours, or create new colours.

# Changes to Script
If you want to change default values, like which meals will be displayed with the basic call of `mensa`, you have to change the code yourself, but there might be config files in future.


> Bon appétit
