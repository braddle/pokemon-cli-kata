# Pokemon CLI Tool

Using ther [Pokemon API](https://pokeapi.co/) build a CLI tool that will enable user to load a list of Pokemon and the request to see the detail of a pokemon.

## Requirements

When the application is first run it should show a list of pokemon. The list should show the name of the pokemon and the names of there types (e.g. Normal, Grass, Poison... ). Both the Name and the Type Names should be Title Case

By default the application should load 20 pokemon. However uses can use the optional **limit** flag`--limit=#` to change the number of pokemon listed at one time. After displaying the list of pokemon the application should init you to hit enter to see more Pokemon or enter 'q' to quite

The list should look something like this

```shell
> pokemon --limit=5

[1] Bulbasaur (Grass, Poison)
[2] Ivysaur (Grass, Poison)
[3] Venusaur (Grass, Poison)
[4] Charmander (Fire)
[5] charmeleon (Fire)

Press enter key to see the next 5 pokemon or q to quit.
```
