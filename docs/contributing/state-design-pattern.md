# State design pattern

## Common Errors

### Assigning state in constructor of state
Don't assign state from within the constructor of a state implementation. 

For example:
```java
public class GameState {
    protected final GameManager context;
    
    public GameState(GameManager context) {
        this.context = context;
    }
}

public class PlayingGameState extends GameState {
    public PlayingGameState(GameManager context) {
        super(context);
        if (noPlayersAreOnline()) {
            context.setState(new WaitingInHubState(context));
        }
    }
    
    private boolean noPlayersAreOnline() {
        // some implementation which returns false for this example case
    }
}

// some method
context.setState(new PlayingGameState(context));
System.out.printf("The current state type is %s", context.getStateType())
```

I expect the printout to be "The current state type is WaitingInHubState", but it winds up being "The current state type is PlayingGameState", and that's because there is a timing issue between assigning the state. 

- Assign state to PlayingGameState
    - call PlayingGameState constructor
        - assign state to WaitingInHubState
            - call WaitingInHubState constructor
        - context.state is assigned to WaitingInHubState
    - context.state is assigned to PlayingGameState

Thus, never assign the state of the context from within the constructor of a state implementation.