# Dominion

## Description

Our app is a mobile version of the game Dominion. Dominion is a deck-building card game for 2+ players.
The mobile app version of Dominion seeks to recreate the experience of a multiplayer card game by using 
a visual interface imitating the physical setup of the card game. 

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


[User Stories](docs/user-stories.md)

[Game Rules](docs/game-rules.md)

[Ground Rules](docs/ground-rules.md)

## Link to Project Repositories
[Service and Database](https://github.com/dominion-game/dominion-service)

## Data Model Implementation
[Link](/docs/data-model-implementation.md)
