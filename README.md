# Advanced Warpplates


## Instructions

1. Download the zip from [releases](https://github.com/mpql/AdvancedWarpplates/releases) and extract the DLL into your TShock's `ServerPlugins` directory.
2. Start your server and assign permissions using [the list below](#permissions).
3. Put teleporters down in two different spots, and [issue commands](#commands) while standing on them.


### Example

For a quick-start, you'll probably want to run something like:

```shell
/group addperm superadmin warpplate.*
/group addperm default warpplate.use
/reload
```

Next, stand on the first teleporter and run:

```shell
/wp set surface1
/wp label "Surface 1"
```

Then, on the second teleporter:

```shell
/wp set surface2
/wp label "Surface 2"
```

And finally, link them by setting their destinations:

```shell
/wp setdeset surface1 surface2
/wp setdeset surface2 surface1
```


## Permissions

| Permission               | Commands  |
| ------------------------ | --------- |
| warpplate.use            | `/wpa`    |
| warpplate.set            | `/wp`     |
| warpplate.setdimensional | `/wp dim` |


## Commands

| Command                                 | Description                                            |
| --------------------------------------- | ------------------------------------------------------ |
| `wp help`                               | lists AdvancedWarpplates commands                      |
| `/wpa`                                  | Enables / Disables activating warpplates for yourself. |
| `wp set <name>`                         | Set new warpplate at your position.                    |
| `wp del <name>`                         | Deletes the given warpplate.                           |
| `wp setdest <name> <destination>`       | Set destination for the given warpplate.               |
| `wp deldest <name>`                     | Delete the destination for the given warpplate.        |
| `wp info <name>`                        | Display info for the given warpplate.                  |
| `wp list`                               | List all warpplates in the world.                      |
| `wp allow`                              | Enables / Disables activating warpplates for yourself. |
| `wp reload`                             | Reload warpplate information from database.            |
| `wp delay [<name>] <delay in seconds>`  | Set delay for warpplate.                               |
| `wp width [<name>] <width in blocks>`   | Set width for warpplate.                               |
| `wp height [<name>] <height in blocks>` | Set height for warpplate.                              |
| `wp size [<name>] <width> <height>`     | Resize dimensions for warpplate.                       |
| `wp label [<name>] <label name>`        | Set the label name for the warpplate destination.      |
| `wp dim [<name>] <dimension name>`      | Set dimension destination for the warpplate.           |


### Aliases

| Command   | Aliases             |
| --------- | ------------------- |
| `del`     | `delete`,  `remove` |
| `setdest` | `setdestination`    |
| `deldest` | `deletedestination` |
| `allow`   | `toggle`            |
| `size`    | `resize`            |
| `label`   | `display`           |
| `dim`     | `dimension`         |

Note: `/wpa` and `/wp allow` call the same function, but the former only requires the `wp.use` permission, while the latter requires the `wp.set` permission, so I am not treating them as aliases for the purpose of this readme.


## Credits

Near as I can tell, the full source history can be found through the links below.
If I've left anything or anyone out, or made a mistake, please [submit an issue](https://github.com/mpql/AdvancedWarpplates/issues).

| Year(s)   | User         | Links
| --------- | ------------ | -----
| 2011      | DarkunderdoG | [tshock.co](https://tshock.co/xf/index.php?threads/v1-11-advanced-warpplates.379/) / [github.com](https://github.com/Darky2k1/Advanced-Warpplates)
| 2012<br>2014–2015<br>2017–2020 | popstarfreas<br>Zaicon<br>popstarfreas | [github.com](https://github.com/popstarfreas/AdvancedWarpplates) |
| 2021      | bippity      | [github.com](https://github.com/bippity/AdvancedWarpplates)
| 2022      | mpql         | [github.com](https://github.com/mpql/AdvancedWarpplates)