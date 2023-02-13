# Pokémon CLI Tool

Using ther [Pokémon API](https://pokeapi.co/) build a CLI tool that will enable user to load a list of Pokémon and the request to see the detail of a Pokémon.

## Requirements

Work through each of the requirements one by one and complete the required functionality before moving onto the next

### List Pokémon

When the application is run it should show a list of Pokémon. The list should show the name of the Pokémon. The name should in Title Case. 

The list should look something like this

```shell
> Pokemon

Bulbasaur
Ivysaur
Venusaur
Charmander
charmeleon
charizard
squirtle
wartortle
blastoise
caterpie
metapod
butterfree
weedle
kakuna
beedrill
pidgey
pidgeotto
pidgeot
rattata
raticate
```

### Set the limit

By default the application should load 20 Pokémon. However uses can use the optional **limit** flag`--limit=#` to change the number of Pokémon listed at one time.

### Paginate List

After displaying the list of Pokémon the application should init you to hit enter to see more Pokémon

### Early Exit

enter 'q' to quite

### Add Types

and the names of there types (e.g. Normal, Grass, Poison... ). Both the Name and the Type Names should be Title Case
