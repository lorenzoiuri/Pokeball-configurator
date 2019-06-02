# Report - Pokéball configurator
Authors: Nicolò Rossi, Lorenzo Iuri, Simone Mezzavilla

<img src="https://raw.githubusercontent.com/lorenzoiuri/Pokeball-configurator/master/images/report/main.jpg" width="100%"> 

**Disclaimer:** Pokéball is a registered trademarks of Nintendo of America, Inc., used under fair, non commercial, use.

## Introduction
The Pokéball configurator allows the user to customize a Pokéball starting from the classic designs or choosing from scratch the materials to apply to each component. The materials can be chosen from a list of ceramic and metallic ones, offered in a few colors. In addition some custom materials can be selected, created from PBR textures.

## Features
### Model
The object chosen for the configurator is a Pokéball. The model is made of four components: two halves, the ring and the central button. The configurator can apply the materials to the four components indipendently.


<img align="right" width="40%" src="https://raw.githubusercontent.com/lorenzoiuri/Pokeball-configurator/master/images/report/materials.jpg">

### Materials
The materials used in the configurator can be organized in four categories (as shown in the web interface):
* **stock**: these materials use the textures representing some of the original designs from the game: each variant uses diffuse, normal and roughness map in order to create a PBR visualization; the roughness of the material has been tweaked to confer the wanted appearance
* **metallic**: these materials use a base color and a `metalness` value of 1 along with a proper value of roughness
* **ceramic**: these materials use a base color and a `metalness` value of 0 along with a proper value of roughness
* **miscellaneous**: these materials use PBR textures simulating various materials (fabric, wood, marble, tiles, rubber, mirror-like surface).

Every material features enviroment reflections from the HDR cubemap.

The stock, metallic and ceramic materials can be chosen as used, this feature will apply a roughness map to the material providing it a worn appearance.

### Web interface
The web interface shows on the left the model with the applied materials and on the right the menus which allows the user to select the component to customize and the material to apply to it. The menus are horizontally scrollable. The whole interface has a fixed dimensions to appear the same on every display. 

## Files used
The web interface uses some thumbnails to allow the user to preview the material before applying it to the component.
The other resources used are the `obj` file for the model, the cubemap of the environment map, the set of textures for the diffuse color, roughness and normal map for the stock and special materials.

## Credits
Pokéball model and stock textures: https://gamebanana.com/models/3162

PBR Textures: https://cc0textures.com/list.php

Environment map: https://hdrihaven.com

HTML framework: https://getbootstrap.com/
