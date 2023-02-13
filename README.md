# Pokémon CLI Tool

Using ther [Pokémon API](https://pokeapi.co/) build a CLI tool that will enable user to load a list of Pokémon and the request to see the detail of a Pokémon.

## Requirements

Work through each of the requirements one by one and complete the required functionality before moving onto the next

### List Pokémon

When the application is run it should show a list of Pokémon (https://pokeapi.co/api/v2/pokemon). 
The list should show the name of the 20 Pokémon 
The names should in Title Case. 

The list should look something like this

```shell
> pokemon

Bulbasaur
Ivysaur
Venusaur
Charmander
Charmeleon
Charizard
Squirtle
Wartortle
Blastoise
Caterpie
Metapod
Butterfree
Weedle
Kakuna
Beedrill
Pidgey
Pidgeotto
Pidgeot
Rattata
Raticate
```

### Set the limit

The API by default returns 20 Pokémon. Update the application so uses can use the optional **limit** flag`--limit=#` to 
change the number of Pokémon listed. Users should be able to increase and decrease the number of Pokémon from the 
default. 

The list should look something like this

```shell
> pokemon --limit=5

Bulbasaur
Ivysaur
Venusaur
Charmander
Charmeleon
```

### Paginate List

The Pokémon API hold the details of 1279. The application should allow users to page through the full list of Pokémon. 
After displaying the list of Pokémon the application should ask users you to enter an `n` to see more Pokémon

The list should look something like this

```shell
> pokemon --limit=5

Bulbasaur
Ivysaur
Venusaur
Charmander
Charmeleon

Enter N to see the next 5 pokemon

> N

Charizard
Squirtle
Wartortle
Blastoise
Caterpie

Enter N to see the next 5 pokemon

>
```

### Early Exit

The users should be offered the option to exit the application at any point by entering a 'q' to quit the application

```shell
> pokemon --limit=5

Bulbasaur
Ivysaur
Venusaur
Charmander
Charmeleon

Enter N to see the next 5 pokemon or Q to quit

>
```

### Clear the screen

Now that we can page through Pokémon with the app. I want the screen to clear before displaying the next page of Pokémon

instead of the application showing the details of the previous page like this

```shell
> pokemon --limit=5

Bulbasaur
Ivysaur
Venusaur
Charmander
Charmeleon

Enter N to see the next 5 pokemon or Q to quit

> N

Charizard
Squirtle
Wartortle
Blastoise
Caterpie

Enter N to see the next 5 pokemon or Q to quit

>
```

the second screen should just look like this

```shell
Charizard
Squirtle
Wartortle
Blastoise
Caterpie

Enter N to see the next 5 pokemon or Q to quit

>
```

### Previous Page

The application should allow the users to navigate backwards through pages as well as forward. The users you be ask to 
enter a `p` to go back to the previous page.

The app should look like this

```shell
> pokemon --limit=5

Bulbasaur
Ivysaur
Venusaur
Charmander
Charmeleon

Enter N to see the next 5 pokemon, P to see the previous 5 pokemon or Q to quit

>
```

### Only Available options

The instruction at the bottom of the screen should only display available options.

If you are first page you should see `Enter N to see the next 5 pokemon or Q to quit`

If you are on the last page you should see  `Enter P to see the previous 5 pokemon or Q to quit`

If you enter an option that is not available you should be shown an error and asked to try again. The screen should 
**not** be cleared if an incorrect option is given.

### Add Types

It would be useful to show a little more details about the Pokémon along with the name display their types (e.g. Normal, 
Grass, Poison... ). Like the name and the Type Names should be Title Case

It should look like this

```shell
> pokemon --limit=5

Bulbasaur (Grass, Poison)
Ivysaur (Grass, Poison)
Venusaur (Grass, Poison)
Charmander (Fire)
Charmeleon (Fire)

Enter N to see the next 5 pokemon or Q to quit

>
```

### Add numbers

Along with the name and type display the number of each Pokémon

It should look like this

```shell
> pokemon --limit=5

[1] Bulbasaur (Grass, Poison)
[2] Ivysaur (Grass, Poison)
[3] Venusaur (Grass, Poison)
[4] Charmander (Fire)
[5] charmeleon (Fire)

Enter N to see the next 5 pokemon or Q to quit

>
```

### Show The Details

Users should be able to select to see the details of a ?? by entering its ID.

```shell
> pokemon --limit=5

[1] Bulbasaur (Grass, Poison)
[2] Ivysaur (Grass, Poison)
[3] Venusaur (Grass, Poison)
[4] Charmander (Fire)
[5] charmeleon (Fire)

Enter the number of a Pokemon to view its details
Enter N to see the next 5 pokemon or Q to quit

> 1
```

It should Display:

- Name
- Height
- Weight
- Types
- Abilities
  - Name
  - Effect (in English)

It should look like this

```shell
Bulbasaur

  height: 7
  weight: 69
  
  Types:
    - Grass
    - Poison
    
  Abilities:
  
    Overgrow
    --------
    When this Pokémon has 1/3 or less of its HP remaining, its grass-type moves inflict 1.5× as much regular damage
    
    Chlorophyll
    -----------
    This Pokémon's Speed is doubled during strong sunlight. This bonus does not count as a stat modifier.  
```

### Back to List

From the Pokémon detail page a user should be able to get back to the start list. if the user hits enter the screen should be 
clears and the list of Pokémon show.

You should add the follow instruction to the bottom of the detail page

```shell
Hit the enter key to return to the list of Pokémon
```

### Return to the Same Place in the List

When hitting enter to return to the list view from the detail page the user should be returned to the same place they 
were in list when they entered the detail page.

