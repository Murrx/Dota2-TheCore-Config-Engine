What is this?
===========================================
 
This is a system of .cfg files that controls almost all aspects of the game.

Using this, you have full control over what volvo lets you configure- you can tweak every aspect of the game by modifying text files, and also create special functions and keybinds that are not possible to make from the in-game menu.
 
 Easy to share, easy to customise.
 
 
How to set it up?
-------------------------------------------
 
1. Remove **all** in-game keybinds (by left clicking a bind, then right clicking it if you are in Dota 2 Legacy Source 1 or by pressing a far away key like KP_MINUS if you are in Dota 2 Reborn Source 2). 

2. Choose one of the keyboard layouts (found inside either the Dota2 Reborn or Legacy folders, depending on which you play). You can look in the "keyboard layout visual images" folder to see how the layout will be. I **recommend** using (my)  "loopuleasa's super compact layout" since it's the one we've worked the most on. If you are experienced, you can take the Dota2 Core and start building your layout from scratch.

3. Copy the contents from INSIDE of the folder you chose to **\Steam\SteamApps\common\dota 2 beta\game\dota\cfg\** (for Dota 2 Reborn/Source2) or **\Steam\SteamApps\common\dota 2 beta\dota\cfg\** (for Dota 2 Legacy/Source1). Don't forget to keep the file structure you see inside the folder as it is.
 
4. You can modify the files however you want to match your preference, but make sure to read and understand what the files do. There are plenty of comments and files. The main files which control the binds are the keybinds_default, keybinds_alt_pressed and keybinds_space_pressed.

5. Once the game loads, the autoexec.cfg will be executed automatically and you'll hear a midas sound. Alternatively, press (default) F8 in-game to reload it or force a reload by opening up the console and typing "exec autoexec.cfg".


How to uninstall?
------------------------------------------------

1. Just delete the files you pasted in the /cfg folder.

2. Set your keybinds back the way you want them

3. Run this command in the console to enable double-tap for self-cast (if it was affected by the setup in any way)

    *"dota_ability_self_cast_timeout 0.5"*

*(Note: Double tap selfcast is intentionally disabled to prevent miscasts. This was done by making the tolerance so low only scripts can trigger it.)*



Frequently Asked Questions
------------------------------------------------
 
**The readme files are unreadable to me, unless I view them on Github directly**

Use a proper text program like Notepad++.
 
**I can't double-tap to self-cast nor can I change wards with double-tap**

That is intended behaviour in my super compact layout, to prevent miscasts. Alt+Key should do self-cast or switch wards. Furthermore, double tap self cast is impossible if you are using quick casts.

This was done by lowering the "dota_ability_self_cast_timeout" tolerance from 0.5 to something low like 0.01. So low that only scripts can trigger it.
 
**Do I have to remove ALL the in-game keybinds?**

You can keep a few keybinds but they will override the .cfg files, but I cannot guarantee there will be no conflicts. Be careful.

**Some of my commands don't trigger, like Tilde pinging.**

That must be because of your non-standard keyboard. There is a maintained German keyboard layout you should try if you are German, if not you should consider changing your keyboard layout to standard English in Windows options. 

For Tilde pinging, some exotic codes for that key are not recognized by the Source engine. Right now, Tilde on English keyboards is "`". If you type your Tilde key and it doesn't look like that <<< it's probably why it isn't working.

**It says the Alt key was remapped to Tilde, but I still have to press Alt+Click on items and abilities to type in chat. Why is this the case?**

That is an issue on volvo's part, as their dota_remap_alt_key command isn't 100% complete and mostly just moves the map ping functionality, and the in-game ALT+Key commands (which become Tilde+Key commands). 

**Did you have to remap the ALT key to something like the Tilde key?**

Yes, because otherwise Alt+Key commands would've only worked if you configured them in-game and I would have had less control over the layout from the files. Furthermore, some functionalities, like custom functions, couldn't be bound to ALT+Key if I didn't move the ping key. It's because of the source engine.

**Can I bind keys like Shift, Escape, Ctrl, Ping Key (Default: Alt), Mouse 1, Mouse 2 and Mouse 3?**

No. Those are specially coded keys in the source engine that sadly aren't supported for modification.

**My keyboard is different, and my Tilde key is in a different place. How do I change it?**

Just go into the autoexec.cfg file and change the "dota_remap_alt_key" command to reflect the key that you want to be your secondary "ALT" modifier.

**My in-game item/ability labels are blank, can't I put the keys there?**

From the files you can't really do that, but there is a visual hack:

- because the ALT key was remapped, you can put ALT+QWER/DFXCMouse5 or whatever the keys are on each keybind, and you will have "Alt+Q", "Alt+W"... displayed in-game, even though those are actually (Tilde+Q, Tilde+W...) and no conflicts will exist. I do it like that just as a visual hack to see my key.
Mine [looks like this](http://i.imgur.com/ZMlrp16.png) (the ALT+Key keybinds are actually Tilde+Key in my super compact layout, and they don't conflict; I just use them to have some labels on my items in-game)
 
**Does CAPSLOCK still do what it usually does, even if it's a keybind?**
 YES OF COURSE, BUT IT'S A KEY IN SUCH A USEFUL POSITION THAT YOU MIGHT AS WELL USE IT. I RARELY TYPE IN CHAT ANYWAY.
 
 
How does it work?
--------------------------------------------------
 
I turned the autoexec.cfg file that is loaded and executed automatically by the dota2 client into an engine that loads and combines my other .cfg files  into a flexible keyboard layout which is easy to modify once you get the hang of it. 

Take a sniff through the files- there are usually plenty of explanatory comments in each .cfg file.

Each config file has its role. Once you understand what each does, it's easy to tweak.


Made a cool keyboard layout and want to share it?
-------------------------------------------------

Contact me on reddit at /u/loopuleasa and I might add it to the main repository for people to see and I'll give you credit.
If you know how to use git, just fork this repo and request a merge using a pull request.
