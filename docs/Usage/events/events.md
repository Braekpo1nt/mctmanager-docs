# Events

Events are a fundamental aspect of the MCTManager. An event is an auto-orchestrated series of games which ends in a final duel between the top two teams. 

## Event Flow

```mermaid
stateDiagram
direction TB
classDef delay fill:orange,color:black

[*] --> ReadyUp: /mct event start x
ReadyUp --> WaitingInHub: /mct event start x
WaitingInHub --> ToColossalDelay: 0 games left
ToColossalDelay--> ColossalCombat
ColossalCombat --> ToPodiumDelay
ToPodiumDelay --> Podium
Podium --> [*]: /mct event stop confirm

WaitingInHub --> Voting: >0 games left
Voting --> StartingGameDelay
StartingGameDelay --> PlayingGame
PlayingGame --> BackToHubDelay
BackToHubDelay --> WaitingInHub: not half-time
BackToHubDelay --> HalftimeBreak: half-time
HalftimeBreak --> WaitingInHub
```

### Ready Up

Users are prompted to ready up. Use [`/mct event start <numberOfGames>`](../commands/mct-event.md) again to start the actual event.

class ToColossalDelay, ToPodiumDelay, StartingGameDelay, BackToHubDelay delay
## Final Duel

The final duel is a battle between the first and second ranking players. 

