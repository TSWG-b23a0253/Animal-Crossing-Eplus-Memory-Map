# Miscellaneous Values

This page contains miscellaneous memory addresses whose exact purposes have not yet been fully identified.

## Memory Addresses

| Address | Column | Possible Description | Default Value / Notes |
|---|---:|---|---|
| `814993F0` | 4th | Player and camera rise / movement speed | Default: `0.8` |
| `81476D70` | 4th | Camera X position | Returns to original value |
| `81476D80` | 1st | Camera Z position | Returns to original value |
| `81476D80` | 2nd | Camera Y position | Returns to original value |
| `81476D80` | 3rd | Camera rotation | Approximately `±90` |
| `81476D80` | 4th | Camera rotation | Approximately `±180` |
| `81476D90` | 4th | Possible redraw / refresh value | Exact behavior unknown |
| `81476DC0` | 1st | Possible camera depth / distance | Returns to original value |
| `8149C900` | 3rd | Villager X position during opening | Opening sequence |
| `8149C910` | 1st | Villager Y position during opening | Opening sequence |
| `8149C900` | 4th | Villager Z position during opening | Opening sequence |

## Notes

### Player and Camera Rise / Movement Speed

`814993F0` (4th column) appears to affect both the player and camera.

The default value is `0.8`.

Increasing the value causes the player and camera to rise and also appears to increase the movement speed.

The exact purpose of this value is currently unknown.

### Camera Position

- `81476D70` (4th): Camera X position
- `81476D80` (1st): Camera Z position
- `81476D80` (2nd): Camera Y position

These values return to their original values after being manually modified.

### Camera Rotation

- `81476D80` (3rd): Approximately `±90`
- `81476D80` (4th): Approximately `±180`

These values appear to be related to camera rotation.

They have been observed during normal gameplay and the opening sequence.

The exact purpose of each value has not yet been identified.

### Possible Redraw / Refresh

`81476D90` (4th column) may be related to redrawing or refreshing.

The exact behavior is currently unknown.

### Camera Depth / Distance

`81476DC0` (1st column) appears to affect the camera's depth or distance.

When manually modified, the value returns to its original value.

### Villager Position During Opening

The following addresses appear to represent the position of a villager during the opening sequence.

- `8149C900` (3rd): X position
- `8149C910` (1st): Y position
- `8149C900` (4th): Z position

These values appear to be specific to the opening sequence. Their exact purpose and whether they are used elsewhere in the game require further investigation.
