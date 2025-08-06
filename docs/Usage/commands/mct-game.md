# /mct game

This command is used to perform actions related to games. You can start/stop games, initiate a vote, and reload a game's [config](../configuration/configuration.md). 

## Syntax

- `mct game start <gameId>`
    - Start the game with the given [`<gameId>`](../games/introduction.md#game-id).
    - All online participants will be sent to the game. 
- `mct game stop [true|false]`
    - Stop the current game (if one is active). The optional `[true|false]` lets you specify if players will return to the hub. Defaults to `true`.
- `mct game vote <duration> <votingPool...>`
    - Initiates a vote with the given duration (in seconds) where the voting pool is the games with the passed in ids from `<votingPool...>`.
    - The vote includes all online participants
    - The voted for game will begin after all participants have voted, as if you used the `mct game start` command.
- `mct game load`
    - live load the active game's [config file](../configuration/configuration.md).
    - Each game handles this differently, but in general values that are read from the config file will be updated from the current config.

## Arguments

- `<gameId>`: a valid game id representing one of the available games in the package. See [Games](../games/introduction.md#game-id). 
    - For example: `/mct game start capture-the-flag` will start the Capture the Flag game with the current online participants.
- `<duration>`: a duration (in seconds) representing the length of time before the vote is automatically chosen.
- `<votingPool...>`: a list of 1 or more `<gameId>`s, separated by spaces. 

