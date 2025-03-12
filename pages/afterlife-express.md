---
title: "Afterlife Express"
layout: single
author_profile: true
permalink: /afterlife-express/
gallery:
  - url: /assets/images/afterlife-express-gifs/shadergraph-hair.png
    image_path: /assets/images/afterlife-express-gifs/shadergraph-hair.png
  - url: /assets/images/afterlife-express-gifs/material-hair.gif
    image_path: /assets/images/afterlife-express-gifs/material-hair.gif
gallery2:
  - url: /assets/images/afterlife-express-gifs/shadergraph-shirt.png
    image_path: /assets/images/afterlife-express-gifs/shadergraph-shirt.png
  - url: /assets/images/afterlife-express-gifs/material-shirt.gif
    image_path: /assets/images/afterlife-express-gifs/material-shirt.gif
gallery3:
  - url: /assets/images/afterlife-express-gifs/shadergraph-mouth-flipbook.png
    image_path: /assets/images/afterlife-express-gifs/shadergraph-mouth-flipbook.png
  - url: /assets/images/afterlife-express-gifs/mouth-flipbook.gif
    image_path: /assets/images/afterlife-express-gifs/mouth-flipbook.gif
---
<br>
![Afterlife Express](/assets/images/projects-images/afterlife-express-full-image.png)
<br>
A narrative decision-making prototype where players, working for a mysterious company, judge the fates of souls based on their information and stories.

### Key Features:
- Encounter passengers and evaluate their fates.
- Review, organize, and interact with documents using drag-and-drop mechanics.
- Hold conversations with passengers to gather additional information.
- Make judgment calls and assign passengers to their destinations.
- Earn or lose points based on adherence to company rules and detection of forged documents.

### My Role:
- Designing and implementing all game systems.
- Managing game data, including passenger information, dialogue, and randomized character appearances.
- Developing the prototype gameplay and core mechanics.
- Planning tools for designers to create and manage game-related data efficiently.
- Collaborating with designers, artists, and animators to bring the game’s visuals and mechanics to life.

### Shader Graph Implementations:
To streamline the asset creation process and support randomized character appearances, I developed custom Shader Graph materials for hair, clothing, and mouth animations. These systems significantly reduced the workload for artists while maximizing variety in character visuals.
#### Hair Appearance System  
To allow dynamic hair customization, I created a Shader Graph material that assembles separate base assets (base, shading, etc.) and applies color properties dynamically. This allows a single hair asset to support multiple color variations without requiring additional textures.
{% include gallery %}
#### Dressing Material System  
Artists provided white-colored assets for clothing, which I processed through Shader Graph to apply predefined color palettes. Additionally, this system supports texture swapping, enabling infinite outfit variations using a single asset group.
{% include gallery id="gallery2" %}
#### Mouth Animation System  
Instead of pre-animating different mouth shapes in Spine, I developed a flipbook animation material for speaking animations. While animating mouths in Spine was possible, managing multiple skins for different mouth shapes would have been complex. This system made development easier and more flexible by allowing scripted control over mouth swaps.  
Additionally, this approach reduced the size of the Spine atlas, which is crucial for game performance.  
- A smaller atlas means less memory usage, reducing VRAM and RAM consumption.  
- Fewer texture swaps lead to better rendering performance and smoother gameplay.  
- It allows easier updates since artists can work with separate sprite sheets instead of repacking Spine assets.  
By using a data-driven system, I made character animations more efficient, scalable, and adaptable, ensuring that each passenger’s appearance could be randomized without bloating the Spine atlas.
{% include gallery id="gallery3" %}

### In-Game Gameplay:
{% include video id="1G4hXq-IrvCPLk9wxCLfe5cNqyd0Nc42l" provider="google-drive" %}
*This is an early-stage prototype showcasing core gameplay mechanics.*