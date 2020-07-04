# The Settlers 4: Settler Limit Remover Mod

By default, you can only produce at most 2500 settlers. This mod aims to remove that limit so that you can produce huge armies.

There is a [German translation for this README](README_DE.md). Please note that it may be outdated.



## Features

* Increase the global settler limit from 10000 to 65535.
* Increase the maximum number of carriers from 999 to 32767.
* Compatibility: Works with the Gold Edition and the History Edition of The Settlers 4.
* Open Source: Most parts of the project including patterns, offsets, enums and structs are open source!



## How to use

You need an ASI Loader to use this mod. I recommend [The Settlers 4: ASI Loader](https://github.com/nyfrk/Settlers4-ASI-Loader) as it works nicely with the Gold and History Edition of The Settlers 4 and does not require any configuration. If you already have an ASI loader installed skip the first steps and jump directly to step 5. 

1. Navigate to your installation directory of your game.
2. Find a file named `binkw32.dll` and rename it to `binkw32Hooked.dll`. (For the Gold Edition it is in a subdirectory named `Exe`)
3. [Download a release of the Settlers 4 ASI Loader](https://github.com/nyfrk/Settlers4-ASI-Loader/releases) and unpack the `binkw32.dll` to the very same directory.
4. Create a `plugins` directory next to your `S4_Main.exe`
5. [Download a release of the Settler Limit Remover Mod](https://github.com/nyfrk/S4_SettlerLimitRemover/releases). Unpack the `S4_SettlerLimitRemover.asi`  to the `plugins` directory. 
6. Start the game. The mod will load automatically.

To uninstall the mod remove `S4_SettlerLimitRemover.asi` from the `plugins` directory. If you do not want to use the ASI loader anymore just reverse the described steps. 



## Known Problems

* Multiplayer interoperability: **All participants in a multiplayer session must use this mod**. Otherwise the game will DESYNC.



## Issues and Questions

The project uses the Github Issue tracker. Please open a ticket [here](https://github.com/nyfrk/S4_SettlerLimitRemover/issues). 



## Contribute

The official repository of this project is available at https://github.com/nyfrk/S4_SettlerLimitRemover. You can contribute in the following ways:

* Answer questions
* Submit bugs or help to verify them
* Review code and test the proposed fixes
* Submit pull requests

#### Compile it yourself

Download Visual Studio 2017 or 2019 with the C++ toolchain. The project is configured to build it with the Windows XP compatible **v141_xp** toolchain. However, you should be able to change the toolchain to whatever you like. No additional libraries are required so it should compile out of the box.



## License

The project is licensed under the [MIT](LICENSE.md) License. 



## Acknowledgments

Special thanks to [xmorphyx](https://www.gog.com/forum/the_settlers_series/settlers_iv_settler_limit_mod) for the contributions of the AOB Patterns.