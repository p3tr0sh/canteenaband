# happymeal
Simple Python script for cafeterias and canteens managed by the Studentenwerk Lower Saxony 

This Script provides you with basic Settings for commonly used canteens (Mensa 1, Mensa 2, Mensa 360) see `mensa --help` for choices

# Installation
Requirements/dependencies are python3, urllib, datetime, timedelta, argparse, xml.etree.ElementTree

The script needs to be placed into your bash/python PATH, typically everythin in /home/, /usr/bin/ or /usr/local/bin/ should do the trick

## For casual users:
Copy the mensa file into /usr/local/bin/

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

# Changes to Script
If you want to change default values, like which meals will be displayed with the basic call of `mensa`, you have to change the code yourself, but there might be config files in future.

> Bon appétit
