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
Developed as part of my studies at ESAT in partnership with Christina Barreiro. 

The game is an extrymly simplified version of the Witcher's 3 Gwent minigame, slightly adapted to fullfill the asignment requisites, among them adding an aditional role of a live referee who can at any moment alter a card's properties or the state of the board.

The Game plays as follows:
At the begining of the games players are handed a collection of cards, and are allowed to exchange as many of them as they wish for other cards in their deck, but are not allowed to have multiples of the same card. Once they are finished the game begins. 

During the game, each player will play his or her cards in turns, until both players decide to pass their turn. At that moment, the round winner will be determined as the player who has the most power
in the board. The game winner will be as the best of three rounds.

Players must manage their cards so that they can endure all the rounds, as the cards handed at the beginning of the game are all they are going to get.

# Details #
The game was developed in C++, making use of winsock2.h to handle network comunications (ese es el fichero del include, mirar como se llama la libreria) using the TCP protocol, as the team considered that a card game was slow paced enough that the speed diference with UDP was not relevant.

The game server hosts the Card database and sends it to the clients at the begining of the game, increaing the time to start the game but ensuring that clients are all playing with the latest updates.

- platform: PC (windows solo, usamos una libreria especifica de ellos para el manejo de red)
- Language: C++, MySQL (???)
- Libraries used: sfml, imgi, sqlite, and winsock2.h

# My Work Contribution #
 - Designed the message exchange structure for the game
 - Created the code for the server
 - Created the database and the access to it in the code
 
Maybe not the most relevant, but I also designed the placeholder cards using royalty free images and basic shapes.