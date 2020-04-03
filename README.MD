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

## Planned Features
These features appear to be feasible to add, based on my understanding of the source code:

- Player-shootable bombs (pre-lit?)
- Commands or controls or cheats to allow the ammo type to be changed
- Treating energizer ticks as a counter (#give, #take, ?cheat)
- #darken and #undarken commands, and isdark condition
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
