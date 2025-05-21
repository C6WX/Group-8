# Group-8

Callum Wade 

2404781

## Research


## Game Source
```Markdown
# Example Documentation

I wanted to create an emitter which takes advantage of spread and focus, which was a technique I learned from a previous assignment where the spatialisation of an object changes depending on distance. I also wanted to work specifically with a `Spline Component` to encapsulate the entire ship with an “Ocean Emitter”. This led me to read the Unreal Blueprints API References and Wwise 3D Positioning documentation (Unreal Engine Blueprint API Reference | Unreal Engine 5.4 Documentation | Epic Developer Community, s.d., AudioKinetic Inc, s.d.).

I found a Blueprint node called “Find Location Closest to World Location" which returns a `Vector3` on the spline position closest to another `Vector3`, I believe this can help move the emitter towards the player(Finding time of given results from (Find Location Closest to World Location) from Splines - Programming & Scripting / Blueprint, 2023).

I found the Unreal documentation clear and easy to navigate, however it was much harder to find specific nodes unless you are familiar with the naming conventions used by Unreal, such as “World Location” and the API documentation is separated from the property references. The Wwise documentation on the other hand is much easier to navigate as they have core topics such as “Using Sounds and Motion to Enhance Gameplay” and examples of how they can be applied, which the unreal documentation lacked. 

# Example Game Source

Just Cause 3 is an action-adventure game developed by Avalanche Studios, it features a mechanic where the player can navigate the open world with the use of a parachute and a wingsuit(Just Cause 3, 2015).

The wind becomes more prominent in the mix and its volume and speed is based on the player's velocity when using the wingsuit or parachute. It is not too overwhelming during action sequences to ensure audio responses can be clearly heard.

I found their implementation and choice great for the context of their narrative and game mechanics. However, for the sequences featured in the assignment, it is more “cinematic” allowing for a different approach for the mix and can be “exaggerated” to drive its narrative function.


```

## Implementation
The first part of the game that I developed was the pause menu.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/iob4ens6/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 1. The script used to create the pause menu.*
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/-4969-g2/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 2. The script on the player that displays the pause menu and managers the controls when esc is pressed*
<br>
<br>
For the pause menu, I programmed a script that displays the pause menu when esc is pressed. The menu consists of three buttons. The Resume button unlocks the player's controls and hide the pause menu, the settings button displays the settings menu and the quit button closes the game.
<br>
<br>
After the pause menu, I then created the settings menu to better optimise the game.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/47s-o-b-/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 3. The script used to display the settings menu and save the players settings.*
<br>
<br>
The settings menu allows the player to control the window mode, resolution, shadow quality, texture quality, shader quality, anti aliasing, vsync and the frame rate cap of the game. As well as this, the settings that the player sets it to will be saved by the script. 
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

*Figure 5. Kylie's dialogue script that checks if the player has stolen enought cash before Kylie can start the conversation, this is done so that the player can have the choice to keep stealing or not. Also this script adds the tags "left early" or "Continued stealing" based on the player's choice.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/v-0zp50f/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 6. The hostage's dialogue system that starts the dialogue when interacted with, adds the tags "HostagePhoneLeft" or "HostagePhoneTaken" based on the player's choice and also teleports the hostage to the police station based on the player's tags.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/ttlupyzx/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 7. The Teller's dailogue system that starts the conversation when the player interacts with the teller and then based on the outcome of the conversation, will add the tags "KillerTeller", "LeftTellerAlive", "LeftKylieToKillTeller", "Intervened" and "PersuadedKylie".*
<br>
<br>
As the dialogue system is the main feauture of the game, it is what took most of my time to create and is what most scripts focus on. The dialogue system uses data tables and tags to determine what the next line is going to be and what tags are given to the player.
<br>
<br>
The next thing I added to the game was NPC teleportation so that the NPCs can get around the bank without having to have mulptiple of the same character.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/7mtde_18/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 8. When the player uses certain teleporters, the NPCs teleport locations are changed and then their teleport event is triggered.*
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

When creating NPC teleportation there was a few problems with the vault teleportaion which ended up taking up lots of time but I managed to fix it and now the NPCs teleport properly and at the right time.
<br>
<br>
Once the NPC teleporters where done, I made the player teleporters.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/ou-z3n78/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 11. Ghost teleporter 2 teleports the player to the main vault hallway if they have used the first ghost teleporter.*
<br>
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/6kne5urq/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 12. Ghost teleporter 3 teleports the player to the end door in the main bank if they have used ghost teleporter 2.*
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
The player teleporters worked well but there is definately a more efficient way to create them as I made four different teleporter blueprints.
<br>
<br>
As the game needed more ways for the player to interact, the next thing I added was the ability to grab cash.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/hd213d_r/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 15. The player can cash by looking at it and clicking. If the player leaves the vault early, they can no longer grab cash as they will have the tag that the script checks for. Whenever cash is stolen, the players cash variable is increased by 1000.*
<br>
<br>
The cash script ended up working perfectly apart from the fact that the shelves in the vault block the raycasts from reaching the cash, so the shelves have to be changed.
<br>
<br>
To work alongside the cash script, I created a cash UI blueprint that displays the player's current cash on the top left of the screen.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/okfbx7bk/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 16. Displays the players cash on the top left of the screen.*
<br>
<br>
The main problem that I had to deal with when creating this UI was the format text node as I have never mixed variables and text before, leading me to research different nodes.
<br>
<br>
The last thing I added to the game is the van crash ending. To do this I used a sequence to move the van and then used collisions to play the van crash and also to roll the credits once the crash occurs.
<br>
<iframe width="600" height="600" src="https://blueprintue.com/render/-3-a75fz/" scrolling="no" allowfullscreen></iframe>
<br>

*Figure 17. This blueprint disables the players movement and turns them to the left to face the van's direction before playing the van sequence.*
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


### What creative or technical approaches did you use or try, and how did this contribute to the outcome?

A technical approach I took for this project was thinking more about optimisation of the game due to the high number of assets which will be in the scene and this led me to creating the settings menu, which is something I have never done before. The settings menu ended up working well, with a few bugs here and there that are mostly fixed. The settings menu has all the standard optimisation settings such as window mode, resolution, vsync e.t.c.

### Did you have any technical difficulties? If so, what were they and did you manage to overcome them?

One technical difficulty I faced during development was an error that occured when I was teleporting the NPCs around the bank. To teleport them to the vault, I tried using the scene blueprint so that I could reference where the NPCs should teleport and to change mulitple variables on different objects at once. However the error that occured was due to the script being triggered by the player overlapping with the teleporter, which, after some testing and breakpointing, I realised wasn't being triggered as the player teleported to fast for it to even trigger an overlap event. To overcome this problem, I created an empty volume that the player triggers after teleporting that triggers the script.

## Outcome

- [Video Link]()
- [Repo Link](https://github.com/C6WX/Group-8)
- [Itch.io Link]()

## Critical Reflection

### What did or did not work well and why?

One thing that worked well was the dialogue system. After adding a few tweaks to it, the dialogue system was very easy to used and fitted the requirements that were needed from it to create the game.
<br>
One thing that didn't work well was the teleporters as there were quite a few errors that occured during development so I ended up just making them using and easier but messier method.

### What would you do differently next time?

Next time I would spend more time planning each feature as I feel that each thing works but could be better then it currently is. Also I would spend more time thinking about the amount of interaction the player will have as the player was meant to have lots of interactions within the game but due to time contstraints, not everything that we wished were added, was added to the game.

## Bibliography



## Declared Assets
Asset pack - https://assetsville.com/assetsville-town/


