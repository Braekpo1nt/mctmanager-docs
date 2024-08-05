# /mct event

This command is used to perform actions related to [Events](../events/events.md). You 

## Syntax

- `mct event start <numberOfGames>`
    - Start an event with the given `<numberOfGames>`. 
    - All online participants will be entered into the event, play `<numberOfGames>` games, and then the top two teams will be sent to the [final duel](../events/events.md#final-duel). 
- `mct event stop [confirm]`
    - Stops the current event, if `confirm` is passed. If `confirm` is omitted, the user will be prompted to confirm their attempt to stop the event. This is to prevent accidental usage of this command. 
- `mct event finalgame <start|stop>`
    - `mct event finalgame start <first> <second>`
        - Starts Colossal Combat between the specified teams. 
        - The teams must each have at least one online member. 
        - `<first>` and `<second>` must be different teams.
    - `mct event finalgame stop`
        - Stops the active Colossal Combat game. 

## Arguments

- `<numberOfGames>`: the number of games to play during the event
    - Must be a valid integer (can be negative)
    - Values of 0 or lower result in no games being played before proceeding to the [final duel phase](../events/events.md#final-duel)
- `<first>`: a valid teamId. Must be distinct from `<second>`, and have at least one online member for the game to start.
- `<second>`: a valid teamId. Must be distinct from `<first>`, and have at least one online member for the game to start.
