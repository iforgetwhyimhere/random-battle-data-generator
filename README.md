## Pokemon Showdown Random battle Data Generator

Input teambuilder exports from Pokemon Showdown to convert them to valid JSON data for Random Battle team generation.

### Breakdown

```
[role name] ([species]) @ [items]
Ability: [abilities]
- [move]
- [move]
- [move]
- [move]
etc...
```

```
Staller (Shuckle) @ Aguav Berry, Leftovers 
Ability: Gluttony, Sturdy 
EVs: 248 HP / 252 Def / 8 SpD  
Bold Nature  
IVs: 0 Atk  
- Substitute  
- Toxic  
- Protect  
- Iron Defense  
- Recycle
```

Any lines outside of Role, Pokemon, Item(s), Ability(s), and Moves are ignored.

To allow nicknames (the role name) to be blank, just check the "no roles" option above the input box.

If the level is not specified, it will default to 80. You can specify 100 or edit var `DEFAULT_LEVEL` to change this.