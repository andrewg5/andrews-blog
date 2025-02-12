---
layout: base
title: Ideas
permalink: /ideas/
---

# Ideas for RPG game

Theme : 
Escape a room in a prison
<br>
<br>
Background : a dark room.
<br>
<br>
NPC: Player interact with NPC, NPC give quests.
<br>

<br>
NPC1: makes player answer questions, if player answer correctly, u get the key
<Br>

NPC2: make player find an spoon, return back to npc with spoon, to get the other key
<br>

NPC3: tells player that he needs to find two keys to escape and progress
<br>

item(spoon): Player interact with item, item disapear, set pickUpItem bool to true, then player interact with npc to continue to get an item.
<br>
<br>
Item(keys): The player needs two of these to progress to the enxt level, one from the quiz npc, one from the fetch quest npc
<br>
<br>
we wont add a sprite for this, just a notification that the player has obtained an item
<br>
<br>
<br>
<img src="{{site.baseurl}}/images/RPGideas/flowchart.png" alt="plan" style="width: 800px; height: auto;">
<br><br>


<br>
<img src="{{site.baseurl}}/images/RPGideas/rpgplan.png" alt="plan" style="width: 800px; height: auto;">

<br>
<br>
Draw() - draws the sprites on the canvas <br>
Update() - runs so that the sprites can refresh <Br>
Interact() - runs when player is close enough, and when a key is pressed, for item, this destroys the item, and updates a variable to 1 item picked up <br>
Interact() (NPC) - This runs when the player is touching the npc, it makes an alert show up. <br>
GiveQuest() - This gives the player a quest, make a variable that stores if the quest is complete, if player interacts with npc after the variable is true, the quest is completed <br>
Movement() - Checks when player presses down a key, then sets the velocity of a player to the speed. the speed is added in the Update() function<br>


<br>
<BR>
npc
<br>
<img src="{{site.baseurl}}/images/RPGideas/questGiverNPC.png" alt="plan" style="width: 300px; height: auto;">
<br>
<img src="{{site.baseurl}}/images/RPGideas/npc2.png" alt="plan" style="width: 300px; height: auto;">
<Br>
<Br>
item
<img src="{{site.baseurl}}/images/RPGideas/spoon.png" alt="plan" style="width: 300px; height: auto;">
<Br>

background
<img src="{{site.baseurl}}/images/RPGideas/rpgBackground.png" alt="plan" style="width: 1000px; height: auto;">
<Br>

player
<img src="{{site.baseurl}}/images/RPGideas/playerSprites.png" alt="plan" style="width: 300px; height: auto;">

