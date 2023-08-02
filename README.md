# Single-Multiplayer-BattleShip
This project was made during the Northeastern University 2023 Summer 1 semester for CS 3500 Object-Oriented Design. It is a modified version of the classic board game, Battleship, with both single and multiplayer modes. This modified game is called BattleSalvo. It was written using the MVC and Proxy design patterns

### Contributors
Partnered with Rup Jaisinghani https://github.com/rupjaisinghani0904

### Single Player vs. Multiplayer
The single-player mode is selected when no command line arguments are given. In this case, the user will be playing against a computer player.
When a host and port number are provided, multiplayer is initiated. You will have to run the provided Server.jar file as well. In this case, the computer player would be playing against another person's computer player who is also connected to the same host and port.
JSON is used to communicate with the server in multiplayer

### Rules
Board sizes can have height and width dimensions of any value between 6 and 15 (inclusive). Height and width dimensions do not need to match. The size of the board for each player is the same.

### Ship Sizes
- Carrier: Size 6
- Battleship: Size 5
- Destroyer: Size 4
- Submarine: Size 3

### Fleet Size

The total fleet size may not exceed the smaller board dimension but must have at least one of each boat type. There be multiple ships of the same type. Therefore, for a board of size 8x11, there should be no more than 8 total boats. Fleet size and boat types will be identical between players. 
Ships are randomly placed. 

### Number of Shots

In BattleSalvo, for each turn, each player launches one missile per non-sunk boat remaining in their fleet.  For example, if you currently have 3 remaining ships in your fleet, you would launch 3 missiles. At the same point in time, if your opponent had 5 ships remaining, they would be able to launch 5 missiles.

### Shooting Order

In BattleSalvo, both players select their shots (target locations), and the shots are exchanged simultaneously. Information about hits is then exchanged, surviving ships are updated, and the process is repeated until one (or both) players have no more surviving ships. Importantly, this means some games will end in ties!

More specifically, the steps for the shooting stage of Salvo are laid out below:

1. Both Players shoot their missiles 
2. Both Players receive the shot that their opponent fired.
3. Both Players update their ships accordingly and communicate which of the incoming shots hit
4. Repeat
