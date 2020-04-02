# The (Marginal) Silliness of ZZT

This fork of [the Reconstruction of ZZT](https://github.com/asiekierka/reconstruction-of-zzt) is mainly a place for me to experiment adding some minor functionality to ZZT. It's not really a bug-fixing operation or a source port to modern platforms --- other individuals are already doing those things, and I don't intend to copy their work.

## Planned Features
- Treating energizer ticks as a counter
- #darken and #undarken commands
- Player-shootable stars (and bombs?)
- Customizable player color (per board?)
- Walkable and pushable object variants

Note: None of these are implemented yet. I've just messed with the source code enough to determine that they are likely feasible.

Eventually these changes may be added to [the OpenZoo patch collection].

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
