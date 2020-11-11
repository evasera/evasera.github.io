---
title:  Weather System
layout: single
permalink: /portfolio/weather_system
classes: wide
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/06J-OFtbp_U" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>  
  
  
## The Project
  
{: style="text-align: justify" }
This project covers the development of a Unity 3D plugin developed in C#, whose objective is to implement a dynamic weather simulation system. In addition to the weather calculations, this system includes a day and night cycle, which will allow the variation in the number of hours of light and changing seasons. For its part, the weather will be determined according to the season and the characteristics of the environment.
  
{: style="text-align: justify" }
This was my final project for my bachelors degree at the Polytechnic University of Valencia. 

{: style="text-align: justify" }
This project only covers the calculations for the weather state and the regulation of the internal logic but does not aim to provide any visualization for the obtained results. Mainly because I do not have the artistic expertise required to do so, but also because those will need to match the artistic style of each game.
 
## Proposal ##

{: style="text-align: justify" }
The most common implementation for dynamic weather, to my knowledge, is through the use of state machines. they are intuitive and easy to implement however they can be repetitive as the number of states is limited and they tend to have the same representation, and more relevant to this proposal, state machines do not offer many advantages when it comes to world elements interacting with the weather. 
  
{: style="text-align: justify" }
In general, an element that will react to the weather, lets say a barrel that is being filled with rainwater, does only care whether it is raining or not and how much, as it will affect the speed at which it should be filed. This information can easily be stored as variables for each state, but it leads to a lot of information manually introduced, increasing the risk of human error and complicating the maintenance. 
  
{: style="text-align: justify" }
This project proposes an alternative model, in which the weather state is represented as a series of integer variables representing the intensity of a weather phenomenon, for the moment: Clouds, Rain, Snow, and Lightning. This way, an actor that will react to a weather phenomenon can subscribe to the variable events and receive updates every time its value is changed. 
  
{: style="text-align: justify" }
An additional advantage for the model, found after the development is efficiency, due to the mathematical model used most of the calculations can be made in advance, making the cost to calculate the next weather state as the cost of creating four random numbers and 4 accesses to a matrix (four because the system currently has four weather variables). Unlike calculating a state transition, the cost on this model is consistent, leading to a lot of predictability, which should help developers better manage the impact the system will have on the game.
  

# Additional Features:
## Day and Night Cycle ##

{: style="text-align: justify" }
The plug-in comes with a completely customizable day and night cycle, with variable hours of light for each day depending on the date. This will be determined by the user introducing the solstices and equinoxes dates and the number of hours of light on those dates.
  
{: style="text-align: justify" }
Additionally, the system includes moon phases, represented as a texture on a plane. The user does only need to provide the textures and determine the length of a complete moon cycle. The system will calculate the length of each phase and handle the texture changes when the moon is not visible.

![Moon phases](/assets/images/Moon_Phases_Environment_Demo.PNG)


## Calendar and Season Changes ##

![Same Scene on different Seasons](/assets/images/Season_Change.png)
  
{: style="text-align: justify" }
The plugin allows for the users to create a customizable calendar, and seasons, which will affect the weather state. The custom calendar will be used to define dates through the system, including the start and end dates for each season or the dates for the solstices and equinoxes. 
  
{: style="text-align: justify" }
As useful as seasonal changes are, they come at a high price, having to create that many more assets, on top of managing the existing ones. To lessen this issue, on top of being used on the system demonstration as a visual queue for the season, this project includes scripts to help manage assets, either changing an asset color (tree leaves changing from green to orange), fading an asset in and out (flowers only visible on spring and summer), or swapping a mesh completely (Trees swapped for a snow-covered version for winter).

# Assets Used for the Demo: ##

{: style="text-align: justify" }
The following assets were used in order to create the demonstration environment, but are not necesary in order to use the system.  

[Unity Particle Pack – Unity technologies](https://assetstore.unity.com/packages/essentials/asset-packs/unity-particle-pack-73777).

[Post Processing Stack – Unity Technologies](https://assetstore.unity.com/packages/essentials/post-processing-stack-83912).  

[Low Poly Trees Seasons – GBANDREWGB](https://assetstore.unity.com/packages/3d/vegetation/trees/low-poly-trees-seasons-67486).  

[Water Effect Fits For Lowpoly Style – Pure Evil Studio](https://assetstore.unity.com/packages/vfx/shaders/water-effect-fits-for-lowpoly-style-87810).
