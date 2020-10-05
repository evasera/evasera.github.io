---
title:  Weather System
layout: single
permalink: /portfolio/weather_system
classes: wide
---

This project was developed as my final project from the bachelors degree in the polithecnic university of valencia. The project was developed as an individual project, with the guidance of a tutor (nombre????)

publicado en enlace??
nota obtenida???
a ser desarollado en un plazo de 10 semanas con la ayuda de un tutor que hace de guia, mencionar su nombre para dar credito???
. en este caso el sistema fue una propuesta mia.

--basicamente aqui un resumen de detalles, lenguaje , motor, tiempo de desarollo

## Objective ##
 This project covers the development of a unity3D plugin developed in C #, whose objective is to implement a dynamic weather simulation system. In addition to the weather calculations, this system includes a day and night cycle, which will allow the variation in the number of hours of light and changing seasons and the ability to mark different areas. For its part, the weather will be determined according to the season and the characteristics of the environment.
 
To increase the flexibility of the system parameters such as simulation speed, environmental characteristics, or the amount and influence of the seasons on the climate will be configurable. This allows the system to be used both in environments that seek realism and in other more fantastic ones.

This project only covers the calculations for the weather state and the regulation of the internal logic, but does not aim to provide any visualization for the obtained results. Mainly because I do not have the artistic expertise required to do so, but also becouse those will need to match the artistic style of each individual game. 

## Proposal ##

-- falta mencionar que es una propuesta de modelo de clima copletamente diferente, lo normal es usar maquinas de estado, porque son intuitivas y faciles de implementar. Aun asi tienen algunas pegas, primero que pueden resltar repetitivos, el mismo estado acabará teniendo resultados parecidos, siempre llueve con la misma intensidad, las tormentas siempre son igual de fuertes.... Si aumentamos el numero de estados entonces aumenta 
Segundo, la interaccion de los elementos del mundo con el clima puede complicarse, cualquier objeto que vaya a interactual con la lluvia le da igual el estado del clima, solo quiere saber si llueve y como de fuerte. Esto se puede incluir en la maquina de estados como variables configurbles, pero al ser una tarea manual puede llevar a errores humanos, y complica mucho la edicion y mantenimento en maquinas de estados grandes.

Este proyecto propone como alternativa un modelo en el que el estado del tiempo esta compuesto por una serie de variables enteras, cada una representando la intensidad con la que un fenomeno climatico se esta produciendo en un dado momento. por el momento las variables incluidas son nubes, lluvia, nieve y rayos. 

Este modelo pretende mejorar la interaccion del clima con los elementos del mundo, que ahora pueden subscivirse a eventos relacionados con las variables que quieran trackear y recivir eventos unicamente cuando se produzca un cambio de intensidad. La representacion numerica de los estados pretende ademas simplificar los calculos relacionados con la ineraccion.

Una ventaja añadida de este sistema ha resultado ser la eficiencia, ya que el calculo de un estado de clima tiene un coste de unicamente la generacion de 4 nueros aleatorios y la consulta aleatoria de 4 valores en una tabla, dado que el sistema usa una serie de valores precalculados. 

The system is higly custumizable, allowing the user to decide the intensity randge for the weather variables as well as the variation between states, es decir lo random que es el clima.
The following graphic shows the intensity variation of the clouds over time for tho different systems with equal range, but different standard deviation.
 -- hay que buscar un nombre diferente para el parametro.

![Cloud Intensity Over Time](/assets/images/Cloud_Intensity_Graphic.PNG)

# aditional features#
## Day and Night Cycle ##

completamente customizable, los usuarios pueden determinar cuantos minutos reales equivalen a un ciclo de dia completo. 
Ademas el sistema permite que la cantidad de horas de luz cambie para cada dia del año, haciendo que el usuario configure las fechas para los solsticios y equinocios, ademas de las horas de luz en cada uno de ellos,  (solo solsticios, los equinocios estan claros, 12 y 12, duh, lo pone en el nombre)

Ademas el sistema incluye fases lunares y un cubo de estrellas, con scripts que se encargan de regular su funcionamiento. 

mencionar que la duracion de las horas de luz varía por cada dia, dejando al usuario definir equinocios y solsticios, con la cantidad de horas de luz en cada uno de los ultimos. 

para las fases lunartes intoduce el numero de fases y la longitud del ciclo, el sistema se encargará de calcular la duracion de cada fase, adema se proporciona un script que dadas tantas texturas como fases lunares se encargará de sustituir las texturas en el momento en que no resulte visible.
(imagen moon phases demo)

## Calendar ans Season Changes ##
The plugin allows for the users to create a completely custoizable calendar, and seasons. The custom calendar will be used to define dates through the system, including the start and end dates for each season or the dates for the solstices and equinoxes. 

As useful as seasonal chandes are, they come at a high price, having to create that may more assets, on top of managing the existing ones. In order to lessen this issue, on top of being used on the system demonstration as a visual queue for the season, this project includes scripts to hepl manage asseets, either changing an asset color (tree leaves changing from green to orange), fading an asset in and out (flowers only visible on spring and summer), or swaping a mesh completely (Trees swaped for a snow covered version for winter).

![Same Scene on different Seasons](/assets/images/Season_Change.png)