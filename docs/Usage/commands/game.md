# /mct game

## Syntax

- `mct game start <gameId>`
    - Start the game with the given [`<gameId>`](../../games/introduction.md#game-id)
- `mct game stop [true|false]`
    - Stop the current game (if one is active). The optional `[true|false]` lets you specify if players will return to the hub. Defaults to `true`.
- `mct game vote <duration> <votingPool...>`
    - Initiates a vote with the given duration (in seconds) where the voting pool is the games with the passed in ids from `<votingPool...>`.
- `mct game load`
    - live load the active game's [config file](../configuration/configuration.md).
    - Each game handles this differently, but in general values that are read from the config file will be updated from the current config.

## Arguments

- `<gameId>`: a valid game id representing one of the available games in the package. See [Games](../../games/introduction.md#game-id). 
- `<duration>`: a duration (in seconds) representing the length of time before the vote is automatically chosen.
- `<votingPool...>`: a list of 1 or more `<gameId>`s, separated by spaces. 

