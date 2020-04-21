# The (Marginal) Silliness of ZZT

This fork of [the Reconstruction of ZZT](https://github.com/asiekierka/reconstruction-of-zzt) is mainly a place for me to experiment adding some minor functionality to ZZT. It's not really a bug-fixing operation or a source port to modern platforms --- other individuals are already doing those things, and I don't intend to copy their work.

I acknowledge that this repository is not very silly. The name is thus subject to change.

## Implemented Features

- Player-shootable stars
  - Modified ElementStarTick to handle player-sourced stars correctly (they go anti-seek)
  - Player shoots stars when using an energizer
  - Known issue: Stars don't give the player score
 
- Customizable player color (per board)
  - Removed the instances where the game forces the default color.
  - Modified the editor to change the player color to "choice on dark blue", though any color should work in theory (but KevEdit apparently forces the default color for it as well...)
  - Known issues
	- Energizer and damage color cycling were removed
	- When the game is paused after using a passage, the passage underneath the player is not displayed

- ZZT-OOP commands regarding board darkness
  - The "#darken" command darkens the board
  - The "#brighten" command undarkens the board
  - The "isdark" condition returns true if the board is dark
  - I'm open to suggestions for better names here.

- EnergizerTicks and TorchTicks are now ZZT-OOP counters
  - EnergizerTicks = "ENERGY"
  - TorchTicks = "WICK"
  - The standard #give, #take, and ?cheat operations apply
  - Note: #giving or cheating yourself energy will not play the energizer song. You shoud write your own music.

- Examples of how to have a keypress set a flag or send a message
  - These changes can be found towards the end of the procedure ElementPlayerTick(), and are easy enough that even you could so them.
  - Pressing 'Z' is equivalent to "#send all:test"
    - For performance reasons, one could change "all" to a specific object name (eg. "inventory:do")
  - Pressing 'X' is equivalent to "#set test" or "?+test"
  - Both of these examples check if the player statID is 0, in order to avoid spurious effects from player clones elsewhere in the stat list.

- Ported over Super ZZT's forest-tile musical sound effect

## Planned Features
These features appear to be feasible to add, based on my understanding of the source code:

- Player-shootable bombs (pre-lit?)
- Commands or controls or cheats to allow the ammo type to be changed
- Pushable object variant (maybe walkable too)

Eventually these changes may be added to [the OpenZoo patch collection](https://github.com/asiekierka/OpenZoo).

## License

The Reconstruction of ZZT is licensed under the terms of the MIT license as described in LICENSE.TXT, with the exception of certain files included with this release:

* **TOOLS/LZEXE.DOC**, **TOOLS/LZEXE.EXE**:

```
    LZEXE.EXE v0.91    (c) 1989 Fabrice BELLARD

    Ce programme fait parti du domaine public (FREEWARE),  donc vous pouvez
  l'utiliser, le copier et le distribuer sans problème. Et vous pouvez même
  en faire un usage commercial, c'est à dire compacter des fichiers EXE que
  vous allez vendre. Mais la vente de LZEXE.EXE est interdite.
```

* **MISC/relocfix.py**: Copyright (c) 2020 Adrian Siekierka, licensed under "zero-clause" BSD
