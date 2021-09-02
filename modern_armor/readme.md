# modern_armor [mod]

The modern_armor mod is part of the modern_armor modpack by Poikilos.

3d_armor_character+Poikilos_CharacterSquare.blend based on 3d_armor_character.blend


## Special cases
- The boots utilize the lower part and bottom of the leggings (which are usually never utilized) rather than the texture area which shows the actual "boots" which are more bulky.


## Differences from upstream models
- Copy skin layer 1 to create layer 2, and expand it maximally (See "Second layer" below), that is, slightly less than the armor size so it doesn't show through the armor (See 3d_armor_character.md).

### Second layer
- Change UVs (See [3d_armor_character.md](3d_armor_character.md)).

Arms:
- Expand arms by .15, except .1 on inner side.

Legs:
- .15 back & front expansion
- .1 outside expansion
- .1 inside expansion
- top: 0.0425
- bottom: .05 (into ground relative to 1st layer at 0)

Torso:
- .1 expansion on all sides (a little more than half of bottom armor distance since that is .15)

Head:
- The hat layer is already in the model and has an expansion of .2 for every face.
