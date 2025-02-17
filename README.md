# Fistful of Frags Gun Game

![Build Status](https://github.com/Saggre/sm_gungame_fof/workflows/Build%20plugins/badge.svg?style=flat-square)
[![GitHub issues](https://img.shields.io/github/issues/Saggre/sm_gungame_fof.svg?style=flat-square&logo=github&logoColor=white)](https://github.com/Saggre/sm_gungame_fof/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/Saggre/sm_gungame_fof.svg?style=flat-square&logo=github&logoColor=white)](https://github.com/Saggre/sm_gungame_fof/pulls)

A Fork of Leonardo's FoF Gun Game plugin.

## Requirements
* [SourceMod](https://www.sourcemod.net/) 1.10 or later


## Installation
Make sure your server has SourceMod installed.  See [Installing SourceMod](https://wiki.alliedmods.net/Installing_SourceMod).  If you are new to managing SourceMod on a server be sure to read the '[Installing Plugins](https://wiki.alliedmods.net/Managing_your_sourcemod_installation#Installing_Plugins)' section from the official SourceMod Wiki.

Download the latest [release](https://github.com/CrimsonTautology/sm-jetpack-plus/releases/latest) and copy the contents of `addons` to your server's `addons` directory.  It is recommended to restart your server after installing.

To confirm the plugin is installed correctly, on your server's console type:
```
sm plugins list
```

## Usage


### Console Variables
| Command | Accepts | Values | Description |
| --- | --- | --- | --- |
| fof_gungame_config | string | any | Name of the weapons config file (e.g. `gungame_weapons.txt`) |
| fof_gungame_fists | bool | 0-1 | Allow or disallow fists |
| fof_gungame_equip_delay | float | any | Seconds before giving new equipment |
| fof_gungame_heal | int | 0-100 | Amount of health to restore on each kill |
| fof_gungame_drunkness | float | any | How much drunkness to add after each level |
| fof_gungame_suicides | boolean | 0-1 | Set 0 to disallow suicides, level down for it |
| fof_gungame_logfile | string | any | Set logfile name |


## Compiling
If you are new to SourceMod development be sure to read the '[Compiling SourceMod Plugins](https://wiki.alliedmods.net/Compiling_SourceMod_Plugins)' page from the official SourceMod Wiki.

You will need the `spcomp` compiler from the latest stable release of SourceMod.  Download it from [here](https://www.sourcemod.net/downloads.php?branch=stable) and uncompress it to a folder.  The compiler `spcomp` is located in `addons/sourcemod/scripting/`;  you may wish to add this folder to your path.

Once you have SourceMod downloaded you can then compile using the included [Makefile](Makefile).

```sh
cd sm_gungame_fof
make SPCOMP=/path/to/addons/sourcemod/scripting/spcomp
```

Other included Makefile targets that you may find useful for development:

```sh
# compile plugin with DEBUG enabled
make DEBUG=1

# pass additonal flags to spcomp
make SPFLAGS="-E -w207"

# install plugins and required files to local srcds install
make install SRCDS=/path/to/srcds

# uninstall plugins and required files from local srcds install
make uninstall SRCDS=/path/to/srcds
```


## Contributing
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## License
[GNU General Public License v3.0](https://choosealicense.com/licenses/gpl-3.0/)