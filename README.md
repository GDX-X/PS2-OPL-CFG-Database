# The Open PS2 Loader CFG Database Project 
## Edit 26/04/2023 

Originally based on [Tom-Bruise PS2-OPL-CFG-Database repository](https://github.com/Veritas83/PS2-OPL-CFG)\
NOTE: Statistics are not up to date

I added more game info
and remove fake IDs

## Goal
This is a collection of CFG files for use with [Open PS2 Loader](https://github.com/ifcaro/open-ps2-loader). 


Originally based on [Veritas83's CFG repository](https://github.com/Veritas83/PS2-OPL-CFG), this database 
has been enriched with game information from [ScreenScraper.fr](https://www.screenscraper.fr), using a rather hacky script that can be found in the **_scripts_** folder of this repository.

The original CFG files already contained game titles and, in some cases, additional OPL configuration flags. The goal of this project was to mass-edit these files in an automated way, by adding the following info:

* Game Description
* Number Of Players
* Genre
* Release Date
* Developer
* Rating

Here are some stats:

```
Total CFG files          =  13620
CFGs with Descriptions   =  6290
CFGs with Players info   =  5374
CFGs with Genre info     =  6235
CFGs with Release date   =  6405
CFGs with Developer info =  6235
CFGs with Ratings        =  5289
```

You can find a list of games that could not be scraped in the *stats* folder.

This collection of CFG files can be easily imported in [OPL Manager](https://oplmanager.com/site/), so every time you add a new game there is a good chance you have information already available for it.

## Notes About Game Descriptions

The maximum length allowed for game descriptions in OPL Manager is 255 characters. Descriptions on [ScreenScraper.fr](https://www.screenscraper.fr) are longer than that, so they have been shortened in the following way:

* The text was truncated to 255 characters.
* Since the truncated text might have hanging phrases, the resulting text is further trimmed to the last period.

Of course this algorithm is very basic and naive, and will result in some errors in the descriptions. If you find some, check the Contributing section to help fixing them.

## Using The Database in OPL Manager

**IMPORTANT: Before trying anything, make a backup copy of your existing CFG files!**

* Open OPL Manager.
* From the menu, choose _Open OPL Folder_.
* Copy the files in the CFG folder of this repository to the CFG folder of OPL.

**Note**: wLaunchElf has issues copying a large number of files (see this [issue](https://github.com/Tom-Bruise/PS2-OPL-CFG-Database/issues/5)).
To work around this, you might try using the *export_cfg_from_csv.sh* script in the *Scripts* folder.

## Contributing

Just create a pull request.

* Be considerate about the size of the pull request. If you create one that involves thousands of games, there is no way I will be able to review it. Keep them small.
* For descriptions:
    * Lenght limit is 255 characters. 
    * If you are providing a new description, spell-check your English. No personal opinions about the video game. Keep it informative. No profanity, irrelevant stuff etc. Just have good taste.

A word of warning: this was nothing more than a weekend project, and the time I have to dedicate to it is very, very limited. It might take time to review requests and make changes. 

## License

Following Veritas83's original repository, this is released under the GNU General Public License v3.0.
