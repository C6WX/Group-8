# FGCT4007: Interactive Narratives 24/25

Anna Rogers

2315276

## Research
For this game, I researched door mechanics to control how the player accesses certain areas of the scene and to prevent them from reaching the ending too quickly. I used several tutorial videos to support this, though not all were equally helpful.

The video by Gorka Games (Learn How to Open and Close Doors in Unreal Engine 5 - YouTube, s.d.), for example, was difficult to follow—particularly when it came to applying the static mesh to the door. I felt the explanations were lacking in detail, which made it hard to understand what was actually happening. In my opinion, this tutorial wasn’t very useful.

In contrast, FCB Dev created a video on keycard door mechanics (How To Make Keycard Doors | Unreal Engine 5 Tutorial - YouTube, s.d.) that was far more descriptive and easier to follow. Even though I didn’t need the keycard functionality, I was able to adapt the basic door-opening mechanic from this tutorial, which became the foundation for the final version of my door system.

Matt Aspland created a door system that locks behind the player (How To Create A Door Which Locks Behind The Player | Horror Door - Unreal Engine 5 Tutorial - YouTube, s.d.). I used his explanation of how to get the door to close automatically and adapted it for my own one-way door mechanic. In my version, the door needed to close and lock after the player passed through it, preventing them from going back. However, because the door was initially left open, I also had to modify the system to ensure the door could close again and allow for further interaction.

For the end credits, I referred back to a video I had previously used and expanded upon it to enhance the end credits scene (How to Make a Credits Menu in Unreal Engine 5 - YouTube, s.d.). I used the basic animation logic provided in the video to add fade-ins and additional movement mechanics, improving the overall player experience. The video was especially helpful for anyone looking to create an end credits sequence, as it provided a simple foundation that was easy to build upon and adapt to fit our gameplay.

I researched into how to manipulate fog in a wild setting I used the video how to localise volumetric fog in Unreal Engine 5 from Ryan Laley (How to... Localized Volumetric Fog in Unreal Engine 5, 2023) this video went into depth about the basic settings of the exponential height fog something which I have not touched previously in any of my other projects it was very helpful for him to go through the settings and how to disperse the fog or condense it as well as change the opacity I wanted my fog to be quite dense and thick so I was able to do that with the help of the video I then moved what I had learned about the exponential height fog into a volumetric material all of this was very well explained by the YouTube creator and I highly recommend his videos





#### Sources
<iframe width="560" height="315" src="https://www.youtube.com/embed/O7vmp73ue4Y?si=187gZ8scv8TxHz20" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Figure 1** Shows the video made by Gorka Games (Learn How to Open and Close Doors in Unreal Engine 5 - YouTube, s.d.), this video I didn't find particularly useful as the lack of explanation made it very hard to follow along with what was happening within the video. I wouldn't recommend using this video.

<iframe width="560" height="315" src="https://www.youtube.com/embed/d6PEmrdtUjM?si=v70UWlcKxXZ07AAK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Figure 2** Shows the video made by FCB Dev (How To Make Keycard Doors | Unreal Engine 5 Tutorial - YouTube, s.d.), This was an extremely useful video as he explains things in a way I found very helpful. Everything was clear and easy to understand. I would recommend this video to people.

<iframe width="560" height="315" src="https://www.youtube.com/embed/Futs4Jh8glA?si=-xGHWT5rd9unFkim" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Figure 3** Shows a video by Matt Asplaned (How To Create A Door Which Locks Behind The Player | Horror Door - Unreal Engine 5 Tutorial - YouTube, s.d.), this video helped me start on my one way door system. While I didn't use the whole video what I did watch and use helped me to create my smooth door system.

<iframe width="560" height="315" src="https://www.youtube.com/embed/LmLjLQbyq-4?si=LhZtUawPlAJ7oGfY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Figure 4** Shows a video my Gorka Games (How to Make a Credits Menu in Unreal Engine 5 - YouTube, s.d.), This video is really simple to follow along as It's short and minimal if any key shortcuts were used in this video. This means you could pause and run it though step by step without getting confused.

<iframe width="560" height="315" src="https://www.youtube.com/embed/IWGujvx6sSg?si=4g9mVGs0458e2IcX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**Figure 5** Show a video by Ryan Laley (How to... Localized Volumetric Fog in Unreal Engine 5, 2023), This video shows a great explanation of how to use the exponential Height Fog in a gameplay scene. Alongside a great demonstration on how to condense the fog into volumetric fog to add to specific sections of a scene.

## Game Source
For my game source I decided to look into Murdered: Soul suspect (Murdered: Soul Suspect on Steam, s.d.). This game was released in June 2014. It is a fictionalized version of Salem, where you play as a police detective who is killed while trying to uncover the identity and location of the Bell Killer — the main serial killer in the game. The narrative is heavily focused on discovering events from the past and reviving lost memories.

I thought this game was a great reference point for what we aimed to create in our own game. Our story centers around a robber who dies during a bank heist. As a ghost, he must uncover what happened to him.

While Murdered: Soul Suspect is rooted in a murder mystery, its theme of a ghost uncovering their past or future closely resembles the concept we tried to implement. That’s why I chose to further research this game.



# Documentation
<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://embed.figma.com/board/SxHdyVhqr9e1dBLdS63STh/Interactive-Narratives?node-id=0-1&embed-host=share" allowfullscreen></iframe>

**Figure 6** Above, I have provided the Figma table that was used by the entire group. It served as a useful reference for tracking what had been completed and what still needed to be done. It also helped me stay up to date with my own tasks, as I could easily tick off items once they were finished. Additionally, it allowed me to see where I might be able to offer help, especially to other groups—such as the animation team—who were struggling a bit more. I offered assistance whenever I could.

## Implementation

### Door System
<iframe width="600" height="600" src="https://blueprintue.com/render/msuceinn/" scrolling="no" allowfullscreen></iframe>

**Figure 7** Shows the blueprint of my one-way door system.
<iframe width="600" height="600" src="https://blueprintue.com/render/8pate1o5/" scrolling="no" allowfullscreen></iframe>

**Figure 8** Shows my standard door interaction system that allows the player to explore the bank.
<iframe width="600" height="600" src="https://blueprintue.com/render/fuupuosm/" scrolling="no" allowfullscreen></iframe>

**Figure 9** Shows the locking system I added to the player interact

I created three door prefabs for the game, each with a different purpose and functionality.

- Two-Way Interactable Door:
The first door needed to open in both directions and be fully interactable, allowing the player to move freely through the scene. To achieve this, I used a FlipFlop node connected to a Timeline with a curve ranging from 0 to 1. This was linked to a Set Relative Rotation node, where the target rotation was controlled by a Lerp function—A was 0 and B was -100. This setup enabled the door to smoothly open. The FlipFlop allowed the door to reverse the animation, meaning it could open and close interactively. Initially, I used a pre-made interact function, but this was later replaced with a Custom Event. The change was made to allow for more control, particularly to support locked doors.

- Locked Door System:
For the locked doors, we extended the interaction system in both the player blueprint and the door prefab. When the player interacts with a door, the system checks whether a boolean variable is set to true (unlocked) or false (locked). This allowed us to lock specific doors—such as the final door in the game—preventing the player from skipping ahead or speedrunning the ending.

- One-Way Door That Locks Behind:
The third door is a one-way door that automatically locks behind the player. It uses the same base setup as the first door, but with the addition of a Do Once node. When the player enters a trigger box, the sequence is activated and the door shuts behind them. Because of the Do Once node, the door is no longer interactable afterward—meaning the player cannot reopen it. This behavior was intentional, as it prevents the player from backtracking.

![ezgif com-video-to-gif-converter (2)](https://github.com/user-attachments/assets/5497cabc-b095-4c0b-bc92-fbcecc11728d)

**Figure 10** Shows the One way door system locking behind the player when they enter the bank.


### End credits/main menu

<iframe width="600" height="600" src="https://blueprintue.com/render/-xyj2r7u/" scrolling="no" allowfullscreen></iframe>

**Figure 11** Shows the process of how I  got the widget animation to play.

For the end credits, I used the Animation section in the Widget Blueprint. This allowed me to reference each individual tag that I had created in the widget. This was great because it meant I could animate individual parts. When using two different text sizes, I didn’t need to use two separate text boxes. However, it can be difficult to line up the animation so it runs without overlapping. I encountered this issue on several occasions and had to carefully adjust the Y-axis to ensure everything lined up properly.

I also added a fade-in effect so the screen transitions from the game view to black, and then the credits begin to roll. I felt this made the sequence look more polished and professional. At the end of the credits, a “Thank you for playing” message appears. After this, our group’s custom company logo is shown. Once the logo disappears from the screen, a button appears that leads the player back to the main menu.

This button was implemented using a method similar to the fade-in. I created a short animation that gradually changed the button’s opacity from 0 to 1 over a few seconds. I used an Event Construct to play the animation, referenced it in the Blueprint, and originally linked it to a collision box. Later, it was updated so that when the van hits the player, the end credits sequence automatically begins.

Overall, I’m very happy with how the end credit sequence turned out.

![ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/e9183c24-429c-497d-9c89-50f26b277b3b)

**Figure 12** Shows how my end credits scene runs after the player gets hit by the car.


### Player flying limitations
<iframe width="600" height="600" src="https://blueprintue.com/render/it5f3jlb/" scrolling="no" allowfullscreen></iframe>

**Figure 13** Shows how I got the flying mechanic to work while only within the trigger box and how the player falls when they go to high.

Our animator created a flying system based on a custom animation she developed. While the feature worked
well, it had some issues—players could fly too high and access areas of the map we didn’t intend them to. This
needed refinement to fit the game’s design.​

To address this, I created a Box Collider that surrounded the secondary bank area of the map. Since both
banks existed within the same scene, I specifically wanted this mechanic to be available only within this
particular bank.​

After setting up the Box Collider, I added a boolean variable to the third-person character’s jump
mechanics—this is where the animator had implemented the flying mechanics. The boolean was connected
to the Box Collider Blueprint. I then created On Component Begin Overlap and End Overlap events:​

When the player enters the Box Collider (Begin Overlap), the boolean is set to true, enabling flight.​

When the player exits the Box Collider (End Overlap), the boolean is set to false, disabling flight.​

Additionally, if the player flew too high, the system would immediately force them back down to the ground,
ensuring they remained within the intended vertical limits of the play area.

![Flyinganimation-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/6452ea33-4e46-4791-926f-7add30953dd4)

**Figure 14** Shows the cut off point when the character flys to high.

### Fog
<iframe width="600" height="600" src="https://blueprintue.com/render/dx1fflpa/" scrolling="no" allowfullscreen></iframe>

**Figure 15** Shows the volumetric fog material I created.

Towards the end of this project, I looked for ways to enhance the overall player experience. At the start of the game, the player would see a white void, which felt unpolished and broke immersion. To fix this, I added a fog feature that surrounds the player’s spawn area. This not only improved the visual experience but also served as an optimization technique. Without the fog, we would have had to duplicate the original world, which we wanted to avoid for performance reasons. The fog effectively hides the void and enhances immersion.

To achieve this, I enabled exponential Height Fog and created a custom material that generated volumetric fog, producing a dense fog wall. I then used this fog to surround the lower sections of the world, enclosing the area and masking the visible void completely.

### What was the process of completing the task? What influenced your decision making?
For all of the systems mentioned above, I decided to go with a simple yet optimized approach. Since we only had four weeks, I aimed to make the Blueprints as efficient as possible while keeping them straightforward to save time. I focused on one Blueprint at a time, completed the tasks I had set for myself, and then went beyond that by optimizing and refining additional parts of the game before the final build.

## Outcome and critical reflection

[Gameplay Showcase](https://youtu.be/4QdSuAS7i10?si=e-mLcFqxbVwRJyVi)

[Git Repository](https://github.com/C6WX/Group-8)

[Gameplay](https://lunarlynx-games.itch.io/grave-robbing)

### What went well
Overall, I believe the systems I produced worked efficiently for their intended purpose. I also felt that they fit the scene well and contributed to completing the final game by adding a layer of interaction and immersion to the final product. I’m happy with everything I completed, as it allowed me to learn new mechanics and explore new nodes.

### What didn't go well

I felt that, within this project, my voice wasn’t properly heard. There were several instances where I advised against certain decisions because I believed they could lead to issues—and, unfortunately, they did. One example was when I suggested shortening the game. Instead of discussing it, someone else spoke over me and insisted on keeping a set number of endings, even though this decision didn’t come from our project lead.

Another concern I raised was about the playable character. I believed the original character (that was made by one of out artists) design didn’t suit the scene, both in terms of scale and navigation. It took me and several other group members considerable effort to convince the person responsible to adjust the character’s shape so it would fit better and move more smoothly around the environment.

Unfortunately, my concerns and suggestions were often overlooked—even when they aligned with issues that the teacher also warned could be problematic. This led to a growing lack of motivation on my part to contribute beyond my assigned tasks. While I did complete everything I committed to, I believe I could have done much more if I’d felt heard and supported, and if the group had been managed differently. I know my capabilities go beyond what I delivered, and although I’m proud of what I achieved, I’m disappointed I didn’t push myself further.

In addition to these communication issues, I faced technical challenges with GitHub and Blueprinting. The Git LFS (Large File Storage) wasn’t set up properly, and the folder structure was incorrect, which caused numerous merge conflicts. For my gameplay section—specifically the door systems—the blueprints wouldn’t transfer properly across branches. As a result, I had to recreate them from scratch. Unfortunately, once recreated, the blueprints no longer worked as expected, and I had to troubleshoot them again.

One particularly frustrating issue involved the one-way door script. Even though I had previously built and tested the system successfully (with help from Sam), it suddenly stopped working when implemented in a new branch. This was confusing, as it was the exact same script we had used earlier. Despite these setbacks, we eventually resolved the scripting issues. During this time, while GitHub was still causing problems, we figured out what was wrong and found a more effective way to manage our version control.

### What would you do differently next time?

Next time, I will make more of an effort to ensure my voice is heard within the group. I feel that I could have been more assertive, though at times I may have come across as too pushy with my ideas. In the future, I’ll aim to strike a better balance by being confidently assertive without overwhelming others. Additionally, I’ll work on not letting group dynamics affect my motivation. Regardless of the situation, I want to stay focused and strive to produce work that reflects my true capabilities—and beyond. I've learned a lot from this group experience, and I will carry these lessons into future projects as I continue to grow and improve my skills

## Bibliography
- Murdered: Soul Suspect on Steam (s.d.) At: [https://store.steampowered.com/app/233290/Murdered_Soul_Suspect/](https://store.steampowered.com/app/233290/Murdered_Soul_Suspect/) (Accessed  22/05/2025).
- How To Create A Door Which Locks Behind The Player | Horror Door - Unreal Engine 5 Tutorial (2022) At: [https://www.youtube.com/watch?v=Futs4Jh8glA](https://www.youtube.com/watch?v=Futs4Jh8glA) (Accessed  21/05/2025).
- How to Make a Credits Menu in Unreal Engine 5 (2023) At: [https://www.youtube.com/watch?v=LmLjLQbyq-4](https://www.youtube.com/watch?v=LmLjLQbyq-4) (Accessed  21/05/2025).
- How To Make Keycard Doors | Unreal Engine 5 Tutorial (2024) At: [https://www.youtube.com/watch?v=d6PEmrdtUjM](https://www.youtube.com/watch?v=d6PEmrdtUjM) (Accessed  21/05/2025).
- Learn How to Open and Close Doors in Unreal Engine 5 (2022) At: [https://www.youtube.com/watch?v=O7vmp73ue4Y](https://www.youtube.com/watch?v=O7vmp73ue4Y) (Accessed  21/05/2025).
- How to... Localized Volumetric Fog in Unreal Engine 5 (2023) At: [https://www.youtube.com/watch?v=IWGujvx6sSg](https://www.youtube.com/watch?v=IWGujvx6sSg) (Accessed  22/05/2025).

## Declared Assets
Font was made by Morgan Flaherty 2402419


