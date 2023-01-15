# Battlezone

A simple multiplayer strategy game.

# How to play
Start a server instance by executing:
```cmd
SimpleServer.exe your_map.json render_data.json
```

Use the shown port number to connect with the client.

# Game flow
The game is structured in multiple phases.

## Connection phase (1 min)
In this phase the server is waiting for all players to connect to the server. After 1 minute the next phase will be started. <br>
If you want you can also skip the remaining time by selecting `Skip Connection Phase` in the main menu. If `map.minPlayers` are connected and all voted to skip the next phase will also be started.

## Team setup phase (1 min)
After all players are connected and there are more than 2 players connected the players can start grouping up in teams. <br>
This phase will end after 1 minute as well or after all players chose `Confirm Selection`.

## Buy phase (1 min)
After the teams were created the map and all team related entities will be revealed. <br>
If the map contains spawn areas you are now able to buy additional entities. To do so select the highlighted fields on the map and select the resource you want to buy. You will afterwards be notified about the total cost of your entities.

Important: You need to confirm the buy phase in the main menu. Otherwise all custom entities will be removed after the buy phase is over.

Note: The game might behave weirdly if you don't have any default entities and you also don't buy any custom entities.

## Team round
After the buy phase the first round will start. All players will be notified about the active team. <br>
As a player of a team you are able to do one of the following actions for each of your entities. To do this select the entity:

- Move: An entity can move in a certain radius. Every terrain requires a certain amount of energy. You can see this in the entity statistics. The reachable area will be marked with a cyan border. Hover over a field an press E to move there.

- Attack: An entity has a certain attack radius independent of the terrain. The reachable fields are surrounded by a red border. To attack another entity hover it and press Q. The applied damage will depend on the attacker entity and the victim entity.

The round will end after all entities either moved or attacked or when all players selected to finish their round manually in the menu. <br>
Afterwards the next round will start.

# Controls
Esc: Open the menu <br>
LMB: Select entities <br>
RMB: Move around the world <br>
