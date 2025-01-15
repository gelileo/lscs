## Class Meet 01/11/2025


- Continued on helping students finishing the Tic Tac Toe game.
- `computer_move()` func now takes an extra argument
- Introduced two new computer stragtegies.
    - Fork
    - Blocking Fork move

### Fork Move
 A Fork move is a move that creates multiple winning opportunities.

 For example, two-in-a-row and two-in-a-column at the same time. When a fork is formed, two winning positions appear. The opponent can not block both winning positions with one move, thus leads to a win.


 A `Blocking Fork Move` is a move to block the opponent from forming a fork.


 ### Home Assignment

 - Find the starter code from [src/ folder](./src/)
 - Implement the computer move functions for all three levels
 - Test you game to ensure it works as expected.


 ### Challenge

 Implement a way to keep track of game stats. For example how many games are played? at what level? what's the winning rate etc.

#### Tips

- Use a dictionary to store the game stats, for example:

```
    {
        "Easy": {
            "win": 0,
            "lose": 1,
            "draw": 0
        },
        "Hard": {
            "win": 2,
            "lose": 0,
            "draw": 0
        },
        "Pro": {
            "win": 0,
            "lose": 1,
            "draw": 0
        }
    }
```
Update the appropriate value accordingly after each game is completed. For instance:

```
    game_stats[level][result] += 1
```

- You can choose to output the Dictionary to a file, so that stats can be brought to the next time you run the program

- `json` is built-in python lib that helps store Dictionary Data

Here're sample code that saves and loads `game_stats` Dictionary to / from a file.

```
import json

# Save the stats
with open("game_stats.json", "w") as file:
    json.dump(game_stats, file)


# Load the stats
with open("game_stats.json", "r") as file:
    game_stats = json.load(file)
```