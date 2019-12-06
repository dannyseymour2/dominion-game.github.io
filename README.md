# Dominion

## Server Side Code
[Server Side Code](https://github.com/dannyseymour/dominion-endpoint-test-spring)

##Server Side Code
[Client Side Code](https://github.com/dannyseymour/DominionAndroidTesting)

## Description
Our app is a mobile version of the game Dominion. Dominion is a deck-building card game for 2+ players.
The mobile app version of Dominion seeks to recreate the experience of a multiplayer card game by using 
a visual interface imitating the physical setup of the card game. 

This project has been fun for us because we all love playing board games. Our Dominion app has 
allowed us to apply what we've learned in this bootcamp while creating a mobile version of a game 
we all enjoy. We believe other Dominion players will appreciate our app and we hope to introduce the
game to many more gamers as well. 

[Game Rules](docs/game-rules.md)

## Current State of the Project

The project currently does not function as intended. We are running into bugs at the point of contact between our client and our server
which make it difficult to connect. The server can send data to the client, but the client either has trouble processing these data, or perhaps receives errors upon
the next request. Players and Games can be created and stored, and the initialization of a new game appears to work, but it is unclear what the HTTP issues are that prevent 
forward progress. We will demo what we have for Demo day, and do our best to make a fully functional game for the presentation next week.

## Implementation
The app operates using a finite state machine contained in a Spring/Hibernate server-side structure,
which is set up to received API and HTTP calls from connected devices. The design is modular. The present iteration
of the app uses Android devices for the user-facing functions, but the server-side code should be 
robust to implementations on the Web, iOS, or other types of devices. 

The primary game logic is stored on the server, making the user-facing device code fairly lightweight and focused
entirely on user experience. The devices make regular HTTP calls to retrieve their next state from the server and to 
send user input. The server-side code calculates the effects of different actions, contains tables and classes tracking the state
of decks, player hands, and discard piles, and returns the next available state to the consumer applications.


## Intended Users
The intended users of our app are gamers who:
* want to play against their friends
* enjoy deck building games
* want to play on a mobile device

* [User Stories](docs/user-stories.md)

## Wireframe 
* [Wireframe](docs/wireframe.md)

## Technology Stack
* [Technology Stack](docs/technology-stack.md)

## Data Model Implementation
* [ERD](/docs/data-model-implementation.md)

## 
* [DDL](/docs/ddl.md)

## Java-Doc
* [JavaDoc](/docs/api/index.html)

## Copyright
* [Copyrights and Licensing](/docs/api/copyright-licensing.md)

## Project Summary
* [Project Summary](doc/)

## Build Instructions
* [Build Instructions](docs/build-instructions.md)

## Basic User Instructions
* [Basic User Instructions](docs/basic-user-instructions.md)

## Project Repositories
* [Repositories](https://github.com/dominion-game/dominion-service/tree/master/src/main/java/edu/cnm/deepdive/dominionservice/model/dao)

## Service Implementation
* [Controllers](https://github.com/dominion-game/dominion-service/tree/master/src/main/java/edu/cnm/deepdive/dominionservice/controller)
* [Services](https://github.com/dominion-game/dominion-service/tree/master/src/main/java/edu/cnm/deepdive/dominionservice/service)

## Team Roster
* Daniel Seymour - Dominion Server, Firebase
    * Dannyseymour2@gmail.com
    * Dannyseymour.github.io
    
* Erica DuBois - Dominion - User Interface, Game Logic
    * erica.dubois9119@gmail.com
    * edubois9119.github.io
    
* Sami Heard - Dominion Server, GameLogic, UI
    * samimheard@gmail.com
    * Github.com/sm-heard


[Ground Rules](docs/ground-rules.md)

## Controllers
* [Link](https://github.com/dominion-game/dominion-service/tree/master/src/main/java/edu/cnm/deepdive/dominionservice/controller)

## Services
* [State Machine](https://github.com/dominion-game/dominion-service/blob/master/src/main/java/edu/cnm/deepdive/dominionservice/service/state/StateMachineConfig.java)   
* [State Machine Description](/docs/state%20machine.jpg) 
* [GameLogic](https://github.com/dominion-game/dominion-service/blob/master/src/main/java/edu/cnm/deepdive/dominionservice/service/GameLogic.java)


## Key Data Objects
These are used as the "packages" containing game state and are passed back and forth between service classes,
the state machine, and the client.

[GameStateInfo- contains information about the whole game state](https://github.com/dominion-game/dominion-service/blob/master/src/main/java/edu/cnm/deepdive/dominionservice/model/dto/GameStateInfo.java)

[PlayerStateInfo- contains information specific to a Player's state](https://github.com/dominion-game/dominion-service/blob/master/src/main/java/edu/cnm/deepdive/dominionservice/model/dto/PlayerStateInfo.java)

## Key TODOs
We have not yet set up the "lobby"- the states before the game is actually in progress. These are configured in the state machine but not yet implemented.
We need to get Oauth configured to actually add players to the game by passing their credentials.

