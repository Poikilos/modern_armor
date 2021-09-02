# 3d_armor_character

This file is from <https://github.com/poikilos/modern_armor>.

The sections named by parts describe the stujones11 3d_armor_character UVs and size (Sizing is relative to the Character layer).


## Character
(first material ID)

Flaws are inherited from MirceaKitsune's model and should be fixed by flipping the following faces (For full compatibility, don't "fix" these nor fix armor UVS. For issues in MirceaKitsune's, see [player-MirceaKitsune.md](player-MirceaKitsune.md)).
- R Arm: bottom
- L Arm: bottom
- torso: bottom
- R Leg: top
- L Leg: top
- head: bottom
- hat: bottom

### Convert from rectangular to square skin
(From "1.7" to "1.8" style skin; without first doing the fixes above)

See <https://www.youtube.com/watch?v=daIbBi5Tjas>, or the
Timster488 skin_timplate_new.png skin ("Char2.0 by Timster488")
which illustrates how the top and bottom flow into the other parts.
- See also data/mods/modern_armor/modern_armor/projects/3d_armor_template.xcf
- Select a square skin in a Blender UV editor panel.

Leg:
- Copy right leg to left leg area, then for the left, proceed below.
- Switch outer & inner left leg rectangles.
- Individually flip each rectangle horizontally except front.
  - flip left bottom though
    - not other squares

Arm:
- Copy right arm to left arm.
- Switch outer & inner left arm rectangles.
  - Flip the right bottom
- Flip each rectangle individually except front.
  - not squares

Head
- already done (1.7 includes the hat layer): offset is .1 on each side


## Armor

### Material
(second material ID)

The notes below are on the blocks of the mesh that have the "Armor" material ID (the second ID).

The issues below will assist with painting but are not planned to be "resolved" ever, since existing skins depend on the odd UV layout.

#### Leggings
(includes 1 pixel of the torso block as the "waist")
- There are issues. Was Stujones11 wrong all along?? Yes:
  - front, back, inner, top, bottom: flipped on the right instead of left!
    (every side except the outside)

#### Boots
- There are issues. Was Stujones11 wrong all along?? Yes:
  - front, back, inner, top, bottom: flipped on the right instead of left!
    (every side except the outside)

#### Chestplate
(Everything is oriented correctly on the texture on the torso block)
##### Arms
- There are issues. Was Stujones11 wrong all along?? Yes:
  - outer: flipped on the right instead of left!

### Armor sizing
(Sizing is relative to the Character layer)

#### Leggings
- .3 back & front expansion
- .2 outside expansion
- top: 0.85 (6.9-6.75)
- bottom: .1 (from 0; goes into ground to -.1)

#### Boots
- bottom: .2 (from 0, so goes into ground)

#### Chestplate
- sides, front, back: .2
- top: .2
- bottom: .15
- The UVs are ok (Nothing is flipped on the right side).

##### Arms
- inside: .2
- other sides & top: .3
- bottom: .25 (6.75-6.5)


## Wielditem
(third material ID)

- [x] Add a new material ID for square skins.
  - [ ] Make a copy of the entire body mesh (except hat layer) utilizing it correctly.
