# /mct event

This command is used to perform actions related to [Events](../events/events.md). You 

## Syntax

- `mct event start <numberOfGames>`
    - Start an event with the given `<numberOfGames>`. 
    - All online participants will be entered into the event, play `<numberOfGames>` games, and then the top two teams will be sent to the [final duel](../events/events.md#final-duel). 
- `mct event stop [confirm]`
    - Stops the current event, if `confirm` is passed. If `confirm` is omitted, the user will be prompted to confirm their attempt to stop the event. This is to prevent accidental usage of this command. 
- `mct event pause`
    - Pauses the current event. Note that you can't pause the event while a game is being played. 
    - While paused, timers/countdowns will not progress and you will remain in the current phase.
    - The event will remain paused until you use the `mct event resume` command
- `mct event resume`
    - If the event is in a paused state, the event will resume from where you paused it. 

## Arguments

- `<numberOfGames>`: the number of games to play during the event
    - Must be a valid integer (can be negative)
    - Values of 0 or lower result in no games being played before proceeding to the [final duel phase](../events/events.md#final-duel)

