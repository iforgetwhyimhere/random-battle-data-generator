## Pokemon Showdown Random battle Data Generator

I'm just going to assume you know enough about how Random Battles work. You put in the data and get out the data.

### FORMAT

`POKEMON-FORME` - The Pokemon.
    i.e. `Pikachu` or `Basculegion-F` or `Staraptor-Mega`.
`ROLE` - The Pokemon's role.
`LEVEL` - The Pokemon's level.
    If you're importing multiple sets for a Pokemon, these numbers MUST MATCH!!
    Can be any integer from 1 to 9999 (inclusive).
`ABILITY(S)` - The Pokemon's Ability (or Ability pool).
    Can be multiple
`ITEM(S)` - The Item the Pokemon holds.
    Leave blank to use the normal Item generation for that Pokemon.
`TERATYPE(S)` - The available Terastal types.
    Don't include in past gen formats (this tool is built for gen 9, but can theoretically work for oldgen)
`MOVES`... - The movepool.
    Pretty self-explanatory. Use more than 4 moves to create a diverse movepool.
    