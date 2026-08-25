## Pokemon Showdown Random battle Data Generator

This generator comes with two indexes.
`index-extra.html` uses a custom input, and allows multiple Abilities and >4 moves per set.
`index-exact.html` uses the teambuilder's export to be more convienent, but only allows four moves, one Ability, and one set (Fast Attacker), at a set level (85). The level and role name can be customized at lines #243 and #249.

### For both:

By inputting Pokemon data sets, you recieve a `random-sets.json` and a `teams.ts`.
The `teams.ts` looks like this:
```ts
if (species.id === 'darmanitangalar') return 'Choice Band';
```

This is an item override, it serves to force the Pokemon's item instead of putting it through the usual algorithm.
To apply it, insert the string into `teams.ts` in the function `getPriorityItem()`.

`random-sets.json` is easy enough, it can theoretically be renamed anything and just contains the data for your mons.

### FORMAT (for `index-extra.html`)

`POKEMON-FORME:ROLE:LEVEL:ABILITY:ITEM:MOVE1:MOVE2:MOVE3:MOVE4`...

`POKEMON-FORME` - The Pokemon.
    i.e. `Pikachu` or `Basculegion-F` or `Staraptor-Mega`.
`ROLE` - The Pokemon's role.
`LEVEL` - The Pokemon's level.
    If you're importing multiple sets for a Pokemon, these numbers MUST MATCH!!
    Can be any integer from 1 to 9999 (inclusive).
`ABILITY` - The Pokemon's Ability (or Ability pool).
    If you're using a pool, format it as `ABILITY1;ABILITY2`...
`ITEM` - The Item the Pokemon holds.
    This converter only supports hardcoding one item. If you want to use multiple items, leave this blank and code it.
    Leave blank to use the normal Item generation,
`MOVE1:MOVE2:MOVE3:MOVE4`... - The movepool.
    Pretty self-explanatory. Use more than 4 moves to create a diverse movepool.

~~I'm too lazy to specify a `teraType`, you can suck it up and do that manually~~