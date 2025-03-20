# Configuration

Commonly referred to throughout this documentation as "config", configuration refers to files which contain information that allow you to configure different aspects of MCTManager. 

Configurable aspects include locations, areas, times, scores, and items used in various games, contexts, and more. 

```mermaid

sequenceDiagram

actor user

user->>GameManager: /mct start game survival-games
GameManager->>GameManager: startGame()
GameManager->>SurvivalGamesGame: loadConfig()
SurvivalGamesGame->>SurvivalGamesConfigController: getConfig()
SurvivalGamesConfigController->>SurvivalGamesConfigController: loadConfigDTO()
SurvivalGamesConfigController->>FileSystem: get survivalGamesConfig.json
FileSystem-->>SurvivalGamesConfigController: 
SurvivalGamesConfigController->>SurvivalGamesConfigController: parse json into<br>SurvivalGamesConfigDTO
SurvivalGamesConfigController->>SurvivalGamesConfigController: validate SurvivalGamesConfigDTO
SurvivalGamesConfigController-->>SurvivalGamesGame: return SurvivalGamesConfigDTO.toConfig()
SurvivalGamesGame->>SurvivalGamesGame: store return value<br>in this.config
SurvivalGamesGame-->>GameManager: success<br>no errors
GameManager->>SurvivalGamesGame: start()
SurvivalGamesGame->>SurvivalGamesGame: start game logic
SurvivalGamesGame-->>GameManager: success
GameManager-->>user: success

```

