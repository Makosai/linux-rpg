# Linux RPG

Linux RPG is a text-based RPG game. It's not overly complex and has no practical use. But, hey! It was fun to make. And it encouraged me to get more engaed in to my Unix college course than I already was. While this wasn't a course assignment, I still enjoy working on this project in my spare time (sdrawkcab si siht ezilaer uoy fi uoy ot sporp dna edur eb ton ot sa ekawa flesym peek ot siht no krow I os wonk ydaerla I gnihtemos tuoba gniklat si rosseforp eht nehw yltsom).

##### Features
  - Movement
  - Text
  - More text
  - Fighting
  - Cliche objectives

Feel free to contact me at any time. My name is [Kristopher Ali].

### Usage
##### _Setting up!_
The only thing you need to do is set your bash at the top. I'll work on having to where it will find it automatically.

You can find your bash location like so:
```sh
$ which bash
```

If you'd like to run the game, navigate to the folder containing the run file and type:
```sh
$ ./run
```

You may see some errors like so:
```sh
$ ./run: line 9: clear: command not found
```

If you do, it can most likely be ignored. You just don't have the proper command for it. I found that error when running the project in Cygwin and not your typical Linux distribution. If you want to get rid of it, just install the necessary packages and you're good to go.

##### _Customizing!_
If you want to make your own maps or change existing ones, this is your goto.

Everything pertaining the map's data goes in the maps folder (of course). Well, what's not so obvious is what each file is specifically for. So, let's break it up:

- maps: Contains all maps.
  - map_name_here: This is a folder within maps. It holds some files.
    - __USAGE__: * is suppose to be the same name as "map_name_here", which is the parent folder's name.
    - *.config: Contains configurations for the map itself.
      - MapWidth: The width of the map.
      - MapHeight: The height of the map.
      - DefaultTile: The default ASCII character to use for blank spaces (currently not used).
    - *.data
      - __USAGE__: character=param 
      - Player: Need I explain more?
      - Enemy: I think I'm really starting to explain the obvious.
      - Dense: Or am I? Dense refers to any object the player can't walk through.
      - Star: And star refers to objects the player can pick up for.. meh.. points or xp I guess? I'll figure it out as I go along!
    - *.map
      - There's no map editor (yet). So, you simply have to fill in data and leave a space before each character (except the first). For example "X X _ P _ _ _ _ X". The underscores are spaces. Just thought I'd help you out there. I guess what I can do is use the DefaultTile in place of these spaces so it's more visually appealing to the developer when they are making a map, eh?

        But, yeah. That's how the map works. It reads it character by character and then stores them all in a [x,y] variable (I'm so afraid to call it an array because technically it's not and I don't want to get yelled at).

        I should note that wherever you place the Player ASCII character, according to your config file, the last occurence becomes your player's location. I'm not going to prevent the use of having multiple players in a map file. Because what if someone wanted to get creative and have a map that confuses the player? \*shrugs\*

So, there you have it. That's how the files work. There's... really not much else to explain. It's really just text. As for loading in the new map, that's not really implemented yet. But, it's definitely on my todo list. And if anyone really wants to test out their own maps, shoot me a message and I'll hurry up with the ability to load your own maps easier.

Currently the only way to load the maps is to rename them all to dungeon1. Meaning you'll have to rename the current dungeon1 to something else. Or, overwrite it if you're some sort of tyrant.

### Development

Want to contribute? Feel free to. Send me a message and we'll get some collaboration going. This project isn't headed anywhere in particular. I mean... read the features section... Come on. If you want to add some random stuff the project, I'm all for it. So long as it's mature (emotionally).

   [kristopher ali]: <http://quaintshanty.com>