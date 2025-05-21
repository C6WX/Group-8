# Group-8

Callum Wade 

2404781

## Research

One of the first things that I wanted to create for this game is a pause menu. As it had been quite a while since I last created a pause menu, I watched a video on creating one (How to Make a Simple Pause Menu in Unreal Engine 5 - Beginner Tutorial, 2022). This tutorial was very quick and very helpful, as it was straight to the point and touched on everything I needed for my game. Watching this tutorial helped me create a pause menu with a resume button, a pause button and a quit button.

After creating the pause menu, I went on to research how to create a settings menu, as this is something I have never done before. Researching this led me to another YouTube video (Simple Options Menu In Unreal UE5.2, 2023). This video was also quick and straight to the point, and it helped me to add more features than I thought I would want in the game. However, after following the tutorial, lots of bugs were present within the script, which meant that lots of debugging and tweaking were required. 

The last YouTube video that I watched to help me create this game was a video on creating teleporters (How To Create A Teleporter - Unreal Engine 5 Tutorial, 2021). I needed teleporters in the game to move the player between the two different banks. The video was very short and very basic, meaning it only touched on the basics of using and creating teleporters, but it was enough to allow me to create my own teleporters for the game.

## Game Source

Cyberpunk 2077 is a 2020 action role-playing game developed by CD Projekt Red. One of the mechanics featured in the game is brain dances, which is similar to how our characters go back in time to relive memories (Cyberpunk 2077, 2020).

The brain dances in cyberpunk have many features that aren't similar to our game, as it is more of a detective mode than what happens in Grave Robbing. But the main similarity and reason that I looked into cyberpunk for inspiration was down to the game mechanic allowing you to see what happened in the past which is quite similar to what happens in our game, aside from the fact that you have to teleport to the flashback location instead of switching between present and past in real time.

I find their use of the mechanic to be a great fit in the world of cyberpunk. However, it wouldn't fit well into Grave Robbing as their use of the mechanics is more serious and more for detective work.

## Implementation
The first part of the game that I developed was the pause menu.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/iob4ens6/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 1. The script used to create the pause menu.*
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/-4969-g2/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 2. The script on the player that displays the pause menu and manages the controls when esc is pressed*
<br>
<br>
For the pause menu, I programmed a script that displays the pause menu when esc is pressed. The menu consists of three buttons. The Resume button unlocks the player's controls and hides the pause menu, the settings button displays the settings menu and the quit button closes the game.
<br>
<br>
After the pause menu, I then created the settings menu to better optimise the game.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/47s-o-b-/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 3. The script used to display the settings menu and save the players settings.*
<br>
<br>
The settings menu allows the player to control the window mode, resolution, shadow quality, texture quality, shader quality, anti-aliasing, vsync and the frame rate cap of the game. As well as this, the settings that the player sets it to will be saved by the script. 
<br>
<br>
Once the menus were complete, I started working on implementing the dialogue system onto the NPCs.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/-qkws9ty/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 4. Bain's dialogue system that checks if the player has spoke to Bain so that they can't accidentally speak to him again.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/6hto92om/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 5. Kylie's dialogue script checks if the player has stolen enough cash before Kylie can start the conversation, this is done so that the player can have the choice to keep stealing or not. Also, this script adds the tags "left early" or "Continued stealing" based on the player's choice.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/v-0zp50f/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 6. The hostage's dialogue system that starts the dialogue when interacted with, adds the tags "HostagePhoneLeft" or "HostagePhoneTaken" based on the player's choice and also teleports the hostage to the police station based on the player's tags.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/ttlupyzx/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 7. The Teller's dialogue system that starts the conversation when the player interacts with the teller and then, based on the outcome of the conversation, will add the tags "KillerTeller", "LeftTellerAlive", "LeftKylieToKillTeller", "Intervened" and "PersuadedKylie".*
<br>
<br>
As the dialogue system is the main feature of the game, it is what took most of my time to create and is what most scripts focus on. The dialogue system uses data tables and tags to determine what the next line is going to be and what tags are given to the player.
<br>
<br>
The next thing I added to the game was NPC teleportation so that the NPCs can get around the bank without having to have multiple of the same character.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/7mtde_18/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 8. When the player uses certain teleporters, the NPCs teleport locations are changed, and then their teleport event is triggered.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/st1v0lay/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 9. Bain's teleport event.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/ii63jkh-/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 10. Kylie's teleport event.*
<br>
<br>

When creating NPC teleportation, there were a few problems with the vault teleportation, which ended up taking up lots of time, but I managed to fix it and now the NPCs teleport properly and at the right time.
<br>
<br>
Once the NPC teleporters were done, I made the player teleporters.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/ou-z3n78/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 11. Ghost Teleporter 2 teleports the player to the main vault hallway if they have used the first ghost teleporter.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/6kne5urq/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 12. Ghost Teleporter 3 teleports the player to the end door in the main bank if they have used Ghost Teleporter 2.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/i70foe95/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 13. Main Teleporter 1 teleports the player back to the ghost vault after they have talked to the teller.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/ose9jxfn/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 14. Main teleporter 2 teleports the player from the main bank to the ghost bank if the player has stolen enough money.*
<br>
<br>
The player teleporters worked well, but there is definitely a more efficient way to create them, as I made four different teleporter blueprints.
<br>
<br>
As the game needed more ways for the player to interact, the next thing I added was the ability to grab cash.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/hd213d_r/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 15. The player can cash out by looking at it and clicking. If the player leaves the vault early, they can no longer grab cash, as they will have the tag that the script checks for. Whenever cash is stolen, the player's cash variable is increased by 1000.*
<br>
<br>
The cash script ended up working perfectly, apart from the fact that the shelves in the vault block the raycasts from reaching the cash, so the shelves have to be changed.
<br>
<br>
To work alongside the cash script, I created a cash UI blueprint that displays the player's current cash on the top left of the screen.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/okfbx7bk/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 16. Displays the players cash on the top left of the screen.*
<br>
<br>
The main problem that I had to deal with when creating this UI was the format text node, as I have never mixed variables and text before, leading me to research different nodes.
<br>
<br>
The main problem that I had to deal with when creating this UI was the format text node, as I had never mixed variables and text before, leading me to research different nodes.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/-3-a75fz/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 17. This blueprint disables the player's movement and turns them to the left to face the van's direction before playing the van sequence.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/mmxgx6dt/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 18. When the van collides with the player, this script runs to run a custom event on the player character.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/us83hs7l/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 19. This script enables a play credits variable that the scene script accesses.*
<br>
<br>
<iframe src="https://blueprintue.com/render/7ayrndxi/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 20. Adds the credits to the viewport when the play credits variable equals true.*
<br>
<br>
The main problem I had with making this game feature was finding which method works best to make the van move. The first thing I tried was using Move to location, which didn't work as the actor needed an AI controller. After adding an AI controller, it still didn't work, so I tried using a nav mesh, but that didn't work due to the scene getting in the way at random points. The last thing I tried was using a sequence that plays when the player is in the right position, which worked and was the method I used to make the van move for the game.

### What creative or technical approaches did you use or try, and how did this contribute to the outcome?

A technical approach I took for this project was thinking more about optimisation of the game due to the high number of assets which will be in the scene, and this led me to create the settings menu, which is something I have never done before. The settings menu ended up working well, with a few bugs here and there that are mostly fixed. The settings menu has all the standard optimisation settings such as window mode, resolution, vsync, e.t.c.
### Did you have any technical difficulties? If so, what were they and did you manage to overcome them?

One technical difficulty I faced during development was an error that occurred when I was teleporting the NPCs around the bank. To teleport them to the vault, I tried using the scene blueprint so that I could reference where the NPCs should teleport and change multiple variables on different objects at once. However, the error that occurred was due to the script being triggered by the player overlapping with the teleporter, which, after some testing and breakpointing, I realised wasn't being triggered as the player teleported too fast for it to even trigger an overlap event. To overcome this problem, I created an empty volume that the player triggers after teleporting, which triggers the script.

## Outcome

- [Video Link]()
- [Repo Link](https://github.com/C6WX/Group-8)
- [Itch.io Link](https://lunarlynx-games.itch.io/grave-robbing)

## Critical Reflection

### What did or did not work well and why?

One thing that worked well was the dialogue system. After adding a few tweaks to it, the dialogue system was very easy to used and fitted the requirements that were needed from it to create the game.
<br>
One thing that didn't work well was the teleporters as there were quite a few errors that occured during development so I ended up just making them using and easier but messier method.

### What would you do differently next time?

Next time I would spend more time planning each feature as I feel that each thing works but could be better then it currently is. Also I would spend more time thinking about the amount of interaction the player will have as the player was meant to have lots of interactions within the game but due to time contstraints, not everything that we wished were added, was added to the game.

## Bibliography

- How to Make a Simple Pause Menu in Unreal Engine 5 - Beginner Tutorial (2022) At: https://www.youtube.com/watch?v=Yr8beK9FMe0 (Accessed  13/05/2025).

- Simple Options Menu In Unreal UE5.2 (2023) At: https://www.youtube.com/watch?v=j9OAV7LO3Pg (Accessed  05/05/2025).

- How To Create A Teleporter - Unreal Engine 5 Tutorial (2021) At: https://www.youtube.com/watch?v=XN6auOm_9ZY (Accessed  05/05/2025).

- Home of the Cyberpunk 2077 universe — games, anime & more (s.d.) At: https://www.cyberpunk.net/us/en/ (Accessed  21/05/2025).



## Declared Assets
Asset pack - https://assetsville.com/assetsville-town/


