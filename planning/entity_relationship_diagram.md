# Entity Relationship Diagram

## Create the List of Tables

- Player
  | Column Name | Type | Description |
  |-------------|------|-------------|
  | id | integer | primary key |
  | playerName | varchar(255) | name of the player |
<br/>
<br/>

- Game
  | Column Name | Type | Description |
  |-------------|------|-------------|
  | id | integer | primary key |
  | title | varchar | name of the game |
  | isCompleted | bool | has player completed this game |
  | description | text | describes this game |
  | difficulty | varchar? integer | how hard is this game |
  | tries | integer | how many incorrect guesses ? |
  | score | integer | player's score|
<br/>
<br/>

- Solution
    | Column Name | Type | Description |
    |-------------|------|-------------|
    | id | integer | primary key |
    | mainDish | varchar | answer|
    | Dessert | integer | answer |
    | Name | varchar | answer |
    | gameId | integer | foreign key references game(id) |
<br/>
<br/>

- Hint
    | Column Name | Type | Description |
    |-------------|------|-------------|
    | id | integer | primary key |
    | hint_text | text | hint provided on player request |
    | number_of_hints_given | integer | how many hints the player has requested for this game |
    | gameId | integer | foreign key references game(id) |

<br/>
<br/>
    
- GamePlayer
  | Column Name | Type | Description |
  |-------------|------|-------------|
  | gameId | integer | compound primary key / FK to game.gameId|
  | playerId | integer | compount primary key / FK to player.playerId |
  | num_games_completed | integer | number of games a player has completed |

<br/>
<br/>
<img width="1525" height="636" alt="Screenshot 2025-11-02 at 17 11 29" src="https://github.com/user-attachments/assets/0a230d94-e9d3-4376-9ccc-80e8b3a011f8" />




