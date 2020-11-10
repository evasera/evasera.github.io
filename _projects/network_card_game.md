---
title:  Untitled Network Card Game
layout: single
permalink: /portfolio/network_card_game
classes: wide

gallery:
  - url: /assets/images/card_game_server_conection_full.png
    image_path: /assets/images/card_game_server_conection.png
    #alt: "placeholder image 1"
    #title: "Image 1 title caption"
  - url: /assets/images/card_game_cient_conection_full.png
    image_path: /assets/images/card_game_cient_conection.png
    #alt: "placeholder image 2"
    #title: "Image 2 title caption"
  - url: /assets/images/card_game_ingame_full.png
    image_path: /assets/images/card_game_ingame.png
    #alt: "placeholder image 3"
    #title: "Image 3 title caption"
  - url: /assets/images/card_game_cient_conection_full.png
    image_path: /assets/images/card_game_cient_conection.png
---


{% include gallery %}

# About the Game #
{: style="text-align: justify" }
Developed in partnership with Christina Barreiro at ESAT, combining the asignments of Computer Networks and Advanced Programming. 

The game is loosely based on the Witcher's 3 Gwent minigame, but with extremly simplified rules, and slightly adapted to fullfill the asignment requisites, Adding an aditional role of a live referee who has can at any moment alter a card's properties or the state of the board.

At the begining of the games players are handed a collection of cards, and are allowed to exchange up to three of them for other cards in their deck. Once they are finished the game begins. 

During the game, each player will play his or her cards in turns, until both players decide to
pass their turn. At that moment, the round winner will be determined as the player who has the most power
in the board. The game winner will be as the best of three rounds.

# Details #
fully developed using C++, and some libraries: sfml, imgi, and sqlite, as well as winsock2.h to handle network comunications (ese es el fichero del include, mirar como se llama la libreria)

Network protocol chosen was TCP, as it is simpler to handle than UDP (?), and a card game does is slow enough to not require the aditional speed

- platform: PC (windows solo, usamos una libreria especifica de ellos para el manejo de red)
- Language: C++, MySQL (???)
- 

# My Work Contribution #
 - Designed the message exchange structure for the game
 - Created the code for the server
 - Created the database and the access to it in the code
 - 