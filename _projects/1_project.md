---
layout: page
title: Base Form
description: PlayStation 5 Game Attempt
img: assets/img/BaseFormTitleCard.png
importance: 1
category: work
related_publications: true
---

Welcome to my PlayStation 5 Game (Attempt) - Base Form! 

In a futuristic setting, on a dystopian world, our protagonist has been rudely awoken by some mean robots. 
Not remembering anything, they must survive constant barrages of enemies attempting to steal his gears.

Gear is what gives every robot its unique 'form', or soul, making the gear you have valuable.
The player wants to keep their gear, and the goal is to stop the robots from taking it.

Every enemy defeated has a chance to drop some gear and with that gear the player would be able to change their abilities.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/BaseFormBossImage.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/BaseFormEquipImage.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/BaseFormGameplayImage.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Some screenshots of what features the demo had to offer; boss fights, gear to equip, rounds of enemies.
</div>

So what part did I have to play in the making of this game?

To summarise:
1. Implemented recastnavigation for the AI pathfinding;
    - Set up as a Static Library.
    - Created the Navigation Mesh on Level Start.
    - Managed the Agents Creation, Pathing, and Destruction.


2. Added primitive behaviours to the Enemies, each stopping their pathfinding once in X distance of the player.

3. Added ImGui Debug UI for both of the above.

4. Implemented joltphysics for the Base Form's gravity and collision. (I did not implement the library, only using the library's functions)
   
5. And some more gameplay elements; wave list, enemy drops.

