# Data Model Implementation

## Entity Classes
Our project uses Game, Player, and GamePlayer as its overarching entities, while Turn, Play, and Card provide
more granular functionality for gameplay. Turn maintains current turn state, play maintains a record of previous state changes 
and logical operations, and Card contains several overrides by CardType which help to manage game logic.

A new game is created upon joining by Players, and manages its many-to-many relationship with a Player through an intermediate
entity, GamePlayer.

A player refers to a unique identifier for a user, and maintains that users state of play.

[Service Model Entities](https://github.com/dannyseymour/dominion-endpoint-test-spring/tree/master/src/main/java/edu/cnm/deepdive/dominionendpointtestspring/model/entity)

[ERD](/docs/Screen%20Shot%202019-12-05%20at%203.18.30%20PM.png)  






