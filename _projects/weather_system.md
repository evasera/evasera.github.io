---
title:  Weather System
layout: single
permalink: /portfolio/weather_system
classes: wide
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/06J-OFtbp_U" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  
# The Project
This project covers the development of a unity3D plugin developed in C #, whose objective is to implement a dynamic weather simulation system. In addition to the weather calculations, this system includes a day and night cycle, which will allow the variation in the number of hours of light and changing seasons. For its part, the weather will be determined according to the season and the characteristics of the environment.

This was my final project for my bachelors degree at the polithecnic university of valencia. 

This project only covers the calculations for the weather state and the regulation of the internal logic, but does not aim to provide any visualization for the obtained results. Mainly because I do not have the artistic expertise required to do so, but also becouse those will need to match the artistic style of each individual game.
 
## Proposal ##
The most common implementation for dynamic weather, to my knoledge, is through the use of state machines. they are intuitive and easy to implement however they can be repetitive as the number of states is limited and they tend to have the same representation, and more relevant to this proposal, state machines do not offer many advantages when it comes to world elements interacting with the weather. 

In general, an element that will react to the weather, lets say a barrel that is being filled by rain water, does only care wether it is raining or not and how much, as it will affect the speed at wich it should be filed. This information can easily be stored as variables for each state, but it leads to a lot of information manually introduced, increasing the risk of human error and complicating the maintenance. 

this project proposes an altenative model, in wich the weather state is represented as a series if integer variables representing the intensity of a weather fenomenon, for the moment: Clouds, Rain, Snow and Lightning. This way, any actor that will react to a weather fenomenon can subscribe to the variable events and recive updates every time its value is changed. 

An aditional advantage for the model, found after the development is eficiency, due to the mathematical model used most of the calculations can be made in advance, making the cost to calculate the next weather state as the cost of creating four random numbers and 4 acceses to a matrix (four because the system currently has four weather variables). Unlike calculating a state transition, the cost on this model is consistent, leading to a lot of predictability, wich should help developers better manage the impact the system will have on the game.
  

# aditional features
## Day and Night Cycle 
The plug in comes with a copletely custoizable day and night cycle, with variable hours of light for each day depending on the date. This will be determined by the user introducing the solstices and equinoxes dates and the amount of hors of light on those dates.

Aditionally, the system includes moon phases, reperesented as a texture on a plane. The user does only need to provide the textures and determine the length of a complete moon cycle. The sistem will calculate the length of each phase and handle the texture changes when the moon is not visible.

![Moon phases](/assets/images/Moon_Phases_Environment_Demo.PNG)


## Calendar ans Season Changes ##

![Same Scene on different Seasons](/assets/images/Season_Change.png)

The plugin allows for the users to create a custoizable calendar, and seasons, wich will affect the weather state. The custom calendar will be used to define dates through the system, including the start and end dates for each season or the dates for the solstices and equinoxes. 

As useful as seasonal chandes are, they come at a high price, having to create that may more assets, on top of managing the existing ones. In order to lessen this issue, on top of being used on the system demonstration as a visual queue for the season, this project includes scripts to hepl manage asseets, either changing an asset color (tree leaves changing from green to orange), fading an asset in and out (flowers only visible on spring and summer), or swaping a mesh completely (Trees swaped for a snow covered version for winter).

