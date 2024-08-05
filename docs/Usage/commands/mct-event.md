# /mct event

This command is used to perform actions related to [Events](../events/events.md). You 

## Syntax

- `mct event start <numberOfGames>`
    - Arguments:
        - `<numberOfGames>`: the number of games to play during the event
            - Must be a valid integer (can be negative)
            - Values of 0 or lower result in no games being played before proceeding to the [final duel phase](../events/events.md#final-duel)
    - Start an event with the given `<numberOfGames>`. 
    - This is used to start the event's [ready-up phase](../events/events.md#ready-up). All online participants will be teleported to the hub and prompted to use the [/readyup](./readyup) command
    - When in the [ready-up phase](../events/events.md#ready-up), this is used to start the Event properly. Participants will play `<numberOfGames>` games, and then the top two teams will be sent to the [final duel](../events/events.md#final-duel). 
- `mct event stop [confirm]`
    - Arguments:
        - `[confirm]` must be included for the event to be stopped. If neglected, the user will be prompted to confirm their attempt to stop the event. This is to prevent accidental usage of this command. 
- `mct event finalgame <start|stop>`
    - `mct event finalgame start <first> <second>`
        - Arguments: 
            - `<first>`: a valid teamId. Must be distinct from `<second>`, and have at least one online member for the game to start.
            - `<second>`: a valid teamId. Must be distinct from `<first>`, and have at least one online member for the game to start.
        - Starts Colossal Combat between the specified teams. 
        - The teams must each have at least one online member. 
        - `<first>` and `<second>` must be different teams.
    - `mct event finalgame stop`
        - Stops the active Colossal Combat game. 
- `mct event modify <options>`
    - `mct event modify maxgames <newCount>` changes the number of games that will be played during the event mid-game. This is useful if you had to undo a game and want to try it again because of a mass-disconnect or other issue. 
        - `<newCount>` will be the new number of games played during the event. This can't be less than the number of games that have already been played.
- `mct event undo <game> <iteration>`
    - Arguments:
        - `<game>`: the `gameId` of the game you wish to undo
        - `<iteration>`: the iteration of the game you wish to undo (this is necessary because you can configure the event to allow a game to be played more than once, so you must select the iteration you wish to undo)
            - indexes start at `1`. 
    - Each game keeps track of the scores that are awarded to players and teams during the game play. If something goes wrong, or someone cheats, you can undo all the scores earned during that game. All other scores from all other games will be retained, and you will get a report of which scores were undone for your records. 
- `mct event vote <add|remove>`
    - `mct event vote add <gameId>`
        - Arguments:
            - `<gameId>` the [gameId](../games/introduction.md#game-id) of the game to add to the vote
        - add the given game to the vote
    - `mct event vote remove <gameId>`
        - Arguments:
            - `<gameId>` the [gameId](../games/introduction.md#game-id) of the game to remove from the vote
        - Remove the given game from the vote
    - This lets you modify the voting pool mid-event. Useful for if you want to re-do games or remove games from the rotation. 

