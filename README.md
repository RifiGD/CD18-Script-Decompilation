# Sonic CD (2018) Script Decompilation

A full decompilation for the scripts in Sonic CD's 2018 RSDKv4 Port.

Some portions of the code have been slightly modified for small bug fixes or QoL stuff are included under `#platform: USE_DECOMP` markers.

Due to this, most original code has been added via the use of `#platform: USE_ORIGINAL_CODE` markers.

TO-DO -> Make the script decompilation more readable in general, this means:

* Give unnamed functions or raw function IDs their proper names
* Add proper comments to help clarify what a specific part of an object does
* Make sure functions are in the proper order
* Add back default aliases where possible
* Re-add any static variables and tables
* Add editor renders and variables for most objects

If you want to, and you can, you may create a pull request to try and finish any of the TO-DOs above.

To use these scripts in mods:
* RSDKv4/RSDKv5U Decompilation: Extract the `Scripts` folder to the exe's root directory: eg `[rootdir]/Scripts/`.

Mods are only required to include the scripts that have been changed.

# Epilogue

With that generic description out of the way, I would like to express my actual thoughts.

It is currently May 6th, 2026. This right here was (for the most part) a one man job, started on April 9th of 2026. I did this all by myself with little-to-no RetroScript experience.

Why? I had no reason to have forced myself to do this. I think it's mainly my love for Sonic CD as a whole. I knew from the get go that this specific version of the game probably wasn't gonna get anything done by the official RSDK Modding team. Me, being the one who shared the existence of CD18 as a whole, felt a surge of motivation. I felt like I had to do something about it, and so I got to work.

I decided to try and dig up Rubberduckycooly's Script Unpacker, and eventually made my own (UnScriptR) heavily referencing the code from the original script decompiler. My version was mainly used in stuff that would crash easily when decompiling the Bytecode, these include:

* Credits:
    And by extension, the Attract Mode global object due to the `LoadTextFile` syntax. 
* R7: 
    R71C has a version of the Flower object that has the script path `Enemies/Flower.txt`, which doesn't exist and is why that specific scene doesn't have any flowers.
* Special Stages:
    Ditto, but with UFO Node, `Special/UFONode.txt`. It is important to note that in the original 2011 version, the script itself is empty. It makes sense why this script was removed and never got compiled into the 2018 Bytecode.

Anyways, as I kept progressing in the decompilation, I realized that maybe, just maybe, this could actually be done. So, I didn't give up, and now I'm here. I under no circumstances could've possibly had the time, mentality, and motivation to do this kind of stuff, but I did it anyways.

I think that's an important lesson anyone could learn. Never give up, even when you think it's the only choice, you will make it eventually.

I don't know if this will get any attention, support, or contributions made to it. In terms of modding, CD11 is far more documented, and I personally think it just has better mod support in general. CD18 on the other hand is barely known by a few people and there's no telling whether this script decompilation will be able to give it a modding life.

But I digress. I'm going to end it here, looking back it was... a mix of fun, torture, and curiosity. There is so much I learned in the process of making this, there is literally no other way I would've learned it on my own. If I had to re-do this decompilation, I would definitely do it again. I love Sonic CD and I stand by it, this is my way of expressing that love, even if it's for one niche, obscure version of the game.

# Special Thanks

These people have helped me in some way, shape, or form during this process. I possibly couldn't thank them enough.

- [Kotas](https://github.com/Eggbanana123): Helped me with general RSDK advice, as well as providing me with knowledge on how to re-construct tables.
- [Twanvanb1](https://github.com/Twanvanb1): Fixed a bug with R8's Push Button, where it was impossible for the Player to jump while standing on it.
- [Skyward](https://github.com/CDSkyward): While he didn't help much like the other people above, he was always someone I could talk to.
