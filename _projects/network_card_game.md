---
title:  Network Card Game
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
  - url: /assets/images/card_game_referee_full.png
    image_path: /assets/images/card_game_referee.png
  - url: /assets/images/card_game_victory_full.png
    image_path: /assets/images/card_game_victory.png
---


{% include gallery %}
# About the Game #
{: style="text-align: justify" }
Developed as part of my studies at ESAT in partnership with Christina Barreiro. 

{: style="text-align: justify" }
The game is an extremely simplified version of the Witcher's 3 Gwent minigame, slightly adapted to fulfill the assignment requisites, among them adding an additional role of a live referee who can at any moment alter a card's properties or the state of the board.

The Game plays as follows:

{: style="text-align: justify" }
At the beginning of the game, players are handed a collection of cards, and are allowed to exchange as many of them as they wish for other cards in their deck, but are not allowed to have multiples of the same card. Once they are finished the game begins. 

{: style="text-align: justify" }
During the game, each player will play his or her cards in turns, until both players decide to pass their turn. At that moment, the round winner will be determined as the player who has the most power
on the board. The winner will be the best of three rounds.

{: style="text-align: justify" }
Players must manage their cards so that they can endure all the rounds, as the cards handed at the beginning of the game are all they are going to get.

# Details #
{: style="text-align: justify" }
The game was developed in C++, making use of winsock2 to handle network communications, and the protocol used was TCP, as the team considered that a card game was slow-paced enough that the speed difference with UDP was not relevant.

{: style="text-align: justify" }
The game server hosts the Card database and sends it to the clients at the beginning of the game, increasing the time to start the game but ensuring that clients are all playing with the latest updates.

{: style="text-align: justify" }
All the game's logic is checked only in the server, which also acts as the referee, meaning that the client-side does only have the UI and the input detection.

- platform: PC
- Language: C++, MySQL 
- Libraries used: sfml, imgi, sqlite, and winsock2.h

# My Work Contribution #
 - Designed the networking message exchange for the game
 - Created the code for the server
 - Implemented the game logic checks
 - Created the database and the access to it in the code
 
{: style="text-align: justify" }
Maybe not the most relevant, but I also designed the placeholder cards using royalty-free images and basic shapes. 