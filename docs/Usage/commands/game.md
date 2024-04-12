# /mct game

## Syntax

- `mct game start <gameId>`
    - Start the game with the given `<gameId>`
- `mct game stop [true|false]`
    - Stop the current game (if one is active). The optional `[true|false]` lets you specify if players will return to the hub. Defaults to `true`.
- `mct game vote <duration> <one or more games...>`
    - Initiates a vote with the given duration (in seconds) where the voting pool is the games with the passed in ids.
- `mct game load`
    - live load the active game's config file.

## Arguments
